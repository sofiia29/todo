<script setup>

</script>

<template>
  <div>
    <router-view>
    </router-view>
  </div>
</template>

<style>


body {
  font-family: 'Amatic SC';
  margin: 0;
  background-color: #E2BDF3;;
  overflow-x: hidden;
}

.container {
  width: 1200px;
  margin: auto;
}

@media(max-width: 700px){
  .container{
    width: 100%;
    margin: 20px 0;
  }
  
}
</style>
