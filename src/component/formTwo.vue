<template>
<div>
  <form-helper>
    <div slot="form-header">
      <h1>Review Form</h1>
      <h2>Form Two</h2>
    </div>
    <div slot="form-field">
      <input type="text" placeholder="Name" required />
      <input type="password" placeholder="Password" required />
    </div>
    <div slot="form-control">
    <button v-on:@click="handleSubmit">Login</button>
    </div>
  </form-helper>
  </div>
  </template>

  <script>

 import formHelper from './formHelper' 

export default {
  components:{
     'form-helper': formHelper 
  },
  data () {
    return {

    }
  },
  
  methods:{

  },

  }


</script>