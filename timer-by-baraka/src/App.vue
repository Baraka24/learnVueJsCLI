<template>
  <div id="app">
    <img alt="Tiki" src="./assets/tiki.png">
    <MyTimer></MyTimer>
  </div>
</template>

<script>
import MyTimer from './components/MyTimer.vue'

export default {
  name: 'App',
  components: {
    MyTimer
  },


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
