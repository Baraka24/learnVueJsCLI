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
      jobs: [
        {title: 'Web Designer', id: 1, details: 'Knowlwdge in HTML, CSS'},
        {title: 'Web Developer', id: 2, details: 'Knowlwdge in PHP, JS, SQL'},
        {title: 'Data Analyst', id: 3, details: 'Knowlwdge in Python'},
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.alert {
  padding: 20px;
  background-color: #0c0c3b;
  color: white;
}
</style>
