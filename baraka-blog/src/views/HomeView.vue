<template>
  <div class="home">
    <p ref="p">Hello, Her name is {{ name }} and she is {{ age }} years old.</p>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
import { ref } from 'vue'

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

    const p = ref(null)

    let name = 'Benedicte'
    let age = 18

    const handleClick = () => {
      console.log(p, p.value)
      p.value.classList.add("test")
      p.value.textContent = "Hello world"
    }
    return {name, age, handleClick, p}
  }
}
</script>
