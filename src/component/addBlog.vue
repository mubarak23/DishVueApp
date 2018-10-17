<template>
<div id="add-blog">
  <h2>Add a New Blog</h2>
  <form v-if="!submitted">
  <label>Blog Title</label>
  <input type="text" v-model.lazy="blog.title" required/>
  <label>Blog Content</label>
  <textarea v-model.lazy="blog.content"></textarea>
  <div id="checkboxes">
    <label>SEO</label>
    <input type="checkbox" value="SEO" v-model="blog.categories"/>
    <label>SEM</label>
    <input type="checkbox" value="SEM" v-model="blog.categories"/>
    <label>SMM</label>
    <input type="checkbox" value="SMM" v-model="blog.categories"/>
    <label>Display Ads</label>
    <input type="checkbox" value="Display Ads" v-model="blog.categories"/>
  </div>
  <label>Author:</label>
  <select v-model="blog.author">
    <option v-for="author in authors">{{ author }}</option>
  </select>
  <button v-on:click.prevent="post">Add Blog</button>
  </form>
  <div v-if="submitted">
    <h3>Post Created</h3>
  </div>
  <div id="preview">
  <h3>Preview Blog</h3>
  <p>Blog Title: {{ blog.title}}</p>
  <p>Blog Content:</p>
  <p>{{ blog.content }}</p>
  <p> Blog Categories</p>
  <ul>
    <li v-for="category in blog.categories">{{ category }}</li>
  </ul>
  <p>Author:{{ blog.author }}</p>
  </div>
</div>

</template>

<script>
export default {
  data() {
    return {
      blog: {
        title: '',
        content: '',
        categories: [],
        author: ''
      },
      authors: ['Techarewa', 'Mubarak', 'Wits'],
      submitted: false
    };
  },
  methods: {
    post: function() {
      this.$http
        .post('http://127.0.0.1:8000/post-blog', {
          title: this.blog.title,
          body: this.blog.body,
          author: this.blog.author,
          categories: this.blog.categories
        })
        .then(function(data) {
          console.log(data);
          this.submitted = true;
        });
    }
  }
};
</script>




<style>
</style>
