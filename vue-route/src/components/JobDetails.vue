<template>
    <div class="alert">
        <hr>
      <!-- <strong>xxxx job id is {{  $route.params.id }} </strong> Job. -->
      <strong>xxxx job id is {{  id }} </strong> Job.
      <hr>
      <p>Details</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'JobDetails',
    props: ['id'],//do not work as expected I have to come back here
    data() {
      return {
        id: this.$route.params.id
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