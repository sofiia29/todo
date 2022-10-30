<template>
  <div>
    <Purple_button>edit</Purple_button>
    <Full_card></Full_card>
  </div>
</template>

<script>
import Purple_button from './../purple_button.vue';
import Full_card from './../full_card.vue';
export default {
  name: "home",
  components:{
    Purple_button,
    Full_card
  }
}
</script>

<style scoped>

</style>