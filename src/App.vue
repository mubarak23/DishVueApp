<template>
<div>
<add-blog></add-blog>
</div>
    
</template>

<script>

import addBlog from './component/addBlog';
import showBlog from './component/showBlog';

export default {
  components:{
    'add-blog': addBlog,
    'show-blog': showBlog
  },

  data(){
    return{
    
    }
  },
     
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
