<template>
  <div class="home">
    <!-- <p ref="p">Hello, Her name is {{ name }} and she is {{ age }} years old.</p> -->
    <p >Hello, Her name is {{ name }} and she is {{ age }} years old.</p>
    <button @click="handleClick">Click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name">
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

    /* const p = ref(null) */

    const name = ref('Benedicte')
    const age = ref(18)

    const handleClick = () => {
      /* console.log(p, p.value)
      p.value.classList.add("test")
      p.value.textContent = "Hello world" */
      name.value = 'Zed'
      age.value = 25
    }
    /* return {name, age, handleClick, p} */
    return {name, age, handleClick}
  }
}
</script>
