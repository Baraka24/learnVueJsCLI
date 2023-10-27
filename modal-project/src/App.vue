<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div v-if="showDiv">
      <MyModal header="My header of Modal" text="Some text..okay" theme="sale" />
    </div>
    <button @click="showIt">
      <span v-if="showDiv">Hide</span>
      <span v-else>Show</span>
    </button>
    <div>
      <MyModal>
        <!-- default slot -->
        <h1>My H1 slot</h1>
        <p>My p slot</p>
        <!-- specific slot -->
        <template v-slot:links>
          <a href="tiki.org">Tiki</a>
          <a href="evoludata.com">evoludata</a>
        </template>
      </MyModal>
    </div>

    <!-- <MyModal :header='header' :text="text" /> -->
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import MyModal from './components/MyModal.vue'

export default {
  name: 'App',
  components: {
    /* HelloWorld, */
    MyModal
  },
  data() {
    return {
      header: 'An other header',
      text: 'An other text oh....',
      showDiv: true,
      btnText: 'Hide'
    }
  },
  methods: {
    showIt() {
      this.showDiv = !this.showDiv
    },

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
