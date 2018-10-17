<template>
<header>
    <h2 v-on:click="changeTitle">{{ title }}</h2>
</header>
</template>

<script>
import { bus } from '../main';

export default {
    props:{
      title:{
      type:String
      }
    },
  
  data () {
    return {
    
    }
  },
  methods:{
    changeTitle:function(){
    //this.$emit('changeTitle', "Teasty Spices");
    this.title = 'Teasty Spices';
    bus.$emit('titleChanged', 'Teasty Spices');
    }
  }

}


</script>

<style scoped>
  
  header{
    background:lightgreen;
    padding:10px;
  }

  h2{
  color:#2222;
  text-align:center;
  }


</style>