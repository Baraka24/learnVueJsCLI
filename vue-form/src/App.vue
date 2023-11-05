<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <VueForm />
</template>

<script>

import VueForm from './components/VueForm.vue'

export default {
  name: 'App',
  components: {
    VueForm
  },
  data() {
    return {
      itemName: null,
      itemNumber: null,
      shoppingList: [
        {name: 'biscuits', number: 9}
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
