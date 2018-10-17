<template>
<div>
  <h1>Please Fill out the form</h1>
  <form>
    <div id="form-header">
        <slot name="form-header"></slot>
    </div>
    <div id="form-field">
        <slot name="form-field"></slot>
    </div>
    <div id="form-control">
        <slot name="form-control"></slot>
    </div>
    <div id="useful-link">
      <ul>
        <li><a href="#">Link 1</a></li>
        <li><a href="#">Link 2</a></li>
        <li><a href="#">Link 3</a></li>
        <li><a href="#">Link 4</a></li>
      </ul>
    </div>
  </form>
</div>
</template>

<script>


export default {
  components:{

  },
  data () {
    return {

    }
  },
  
  methods:{

  },

  }


</script>



