<template>
  <div class="home">
    <p>Hello, Her name is {{ name }} and she is {{ age }} years old.</p>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
/*   setup() {
    console.log("Setup");
  },
  created() {
    console.log("Created");
  },
  mounted() {
    console.log("mounted");
  } */
  setup () {
    let name = 'Benedicte'
    let age = 18
    return {name, age}
  }
}
</script>
