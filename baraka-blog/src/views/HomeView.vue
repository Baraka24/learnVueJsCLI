<template>
  <div class="home">
    <!-- <p ref="p">Hello, Her name is {{ name }} and she is {{ age }} years old.</p> -->
    <!-- <p >Hello, Her name is {{ name }} and she is {{ age }} years old.</p>
    <button @click="handleClick">Click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name"> -->
    <input type="text" v-model="search">
    <p>Search name: <b>{{ search }}</b></p>
    <p v-for="name in names" key="name">{{ name }}</p>
  </div>
</template>

<script>
import { ref, computed } from 'vue'

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

   /*  const name = ref('Benedicte')
    const age = ref(18) */

    /* const handleClick = () => { */
      /* console.log(p, p.value)
      p.value.classList.add("test")
      p.value.textContent = "Hello world" */
     /*  name.value = 'Zed'
      age.value = 25
    } */
    /* return {name, age, handleClick, p} */
    /* return {name, age, handleClick} */

    /* const name = computed(() => {
      return "Baraka"
    })
    return { name } */
    const search = ref('')

    const names = ref(['Baraka', 'Boss', 'Bruno', 'Josaphat', 'Domeshow', 'Rodriguez', 'Merci'])

    //const matchingNames = computed()

    return { names, search }
  }
}
</script>
