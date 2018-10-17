<template>
<div id="spice">
  
  <ul>
    <li v-for="spice in spices" v-on:click="spice.show = !spice.show">
      <h2>{{spice.name}}</h2>
      <h3 v-show="spice.show">{{spice.Audience}}</h3>
    </li>
  </ul>
  <button v-on:click="deleteSpice">Delete Spice</button>
  </div>
</template>

<script>
export default {
  props:{
    spices:{
      type:Array,
      required:true
      }
    },

  data () {
    return {
      
    }
  },
  methods:{
      deleteSpice:function(){
        this.spices.pop();
      }
  },

  //life cycle hooks
  beforeCreate(){
    alert("Before Create");
    console.log("Before Created");
  },
  create(){
  alert('Created');
  console.log("Created");
  },
  beforeMount(){
  alert("Before Mount");
  console.log("Before Mount");
  },
  mounted(){
  alert("Mounted");
  console.log("Mounted");
  },
  beforeUpdate(){
    alert('Before Update');
    console.log("Before Update");
  },
  updated(){
    alert('updated');
    console.log('Updated');
  }

}


</script>

<style scoped>
  #spice{
  width:100%;
  max-width:1200px;
  margin:40px auto;
  padding:0 20px;
  box-sizing:border-box;
  }

  ul{
  display:flex;
  flex-wrap:wrap;
  list-style-type:none;
  padding:0;
  }

  li{
    flex-grow:1;
    flex-basis:300px;
    text-align:centre;
    padding:30px;
    border:1px solid #222;
    margin:10px;

  }


</style>