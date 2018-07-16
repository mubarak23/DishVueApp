<template>
  <ul>
    <li v-for="spice in spices">{{ spice }}</li>
  </ul>
</template>

<script>
export default {
  
  data () {
    return {
      spices:['Shawarma', 'Snacks', 'Chicken']
    }
  }

}


</script>

