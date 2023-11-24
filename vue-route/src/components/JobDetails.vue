<template>
    <div class="alert">
        <hr>
      <strong>xxxx</strong> Job.
      <hr>
      <p>Details</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'JobDetails',
    props: {
      msg: String
    },
    data() {
      return {
        
      }
    }
  }
  </script>
<style>
.alert {
  padding: 20px;
  background-color: #0c0c3b;
  color: white;
}
</style>