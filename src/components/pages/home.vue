<template>
  <div class="container">
    <Full_card></Full_card>
  </div>
</template>

<script>
import Full_card from './../full_card.vue';
import axios from 'axios';

export default {
  name: "home",
  components:{
    Full_card,
},
  data(){
    return{
      file: null,
    }
  },
  mounted(){
    axios.get('http://127.0.0.1:54321/').then(response => {console.log(response)})
  }
}
</script>

<style scoped>
  
</style>