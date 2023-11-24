<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'about' }">About</router-link>
    <div>
      <button class="btn success" @click="back">Go back</button>&nbsp;
      <button class="btn info" @click="redirect">Redirect</button>&nbsp;
      <button class="btn warning" @click="forward">Go forward</button>
    </div>
  </nav>
  <router-view/>
</template>

<script>
export default {
 /*  methods: {
    redirect() {
      this.$route.push({ name: 'Home'})
    },
    back() {
      this.$route.go(-1)
    },
    forward() {
      this.$route.go(1)
    }
  } */ //I have to work on them all in its good way
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.success {background-color: #04AA6D;} /* Green */
.success:hover {background-color: #46a049;}

.info {background-color: #2196F3;} /* Blue */
.info:hover {background: #0b7dda;}

.warning {background-color: #ff9800;} /* Orange */
.warning:hover {background: #e68a00;}

.btn {
  border: none;
  color: white;
  padding: 14px 28px;
  font-size: 16px;
  cursor: pointer;
}
</style>
