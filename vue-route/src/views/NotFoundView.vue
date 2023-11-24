<template>
    <div class="home">
      <img alt="Vue logo" src="../assets/logo.png">
      <NotFound/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import NotFound from '@/components/NotFound.vue'
  
  export default {
    name: 'JobDetailsView',
    components: {
     NotFound
    }
  }
  </script>
  