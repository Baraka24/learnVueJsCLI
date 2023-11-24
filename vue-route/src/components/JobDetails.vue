<template>
    <div class="alert" v-for="job in jobs" :key="job.id">
      <strong>{{job.title}}</strong> Job.
      <hr>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    data() {
      return {
        
      }
    }
  }
  </script>