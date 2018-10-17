<template>
<div id="show-blogs">
  <h1>All Blog Articles</h1>
  <div class="single-blog" v-for="blog in blogs">
      <h2>{{blog.title}}</h2>
      <p>{{blog.body}}</p>
  </div>
</div>
    
</template>

<script>


export default {
  

  data(){
    return{
      blogs: []
    }
  },
   

  methods:{

  },

  created(){
      this.$http.get('https://jsonplaceholder.typeicode/post').then(function(data){
          console.log(data);
         this.blogs = data.body.slice(0,10);
      })
  }

}






</script>




<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
  color:purple;

}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
