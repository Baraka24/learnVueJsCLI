<template>
    <div class="home">
      <img alt="Vue logo" src="../assets/logo.png">
      <JobDetails/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import JobDetails from '@/components/JobDetails.vue'
  
  export default {
    name: 'JobDetailsView',
    components: {
     JobDetails
    }
  }
  </script>
  