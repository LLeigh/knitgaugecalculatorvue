<template>
  <div id="app">
      <nav>
        <router-link v-bind:to="{ name: 'welcome' }" >Home</router-link>&nbsp;|&nbsp;
        <router-link v-bind:to="{ name: 'calculator' }">Calculator</router-link>&nbsp;|&nbsp;
        <router-link v-bind:to="{ name: 'about' }">About Me</router-link>
      </nav>
      <router-view> </router-view>
    </div>
</template>

<script>

export default {
  name: 'App',
  components: {

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
  margin-bottom: 60px
}
#nav {
  padding: 30px;
  text-align: center;
}

#nav a {
  font-weight: bold;
  color: #371950;
}

#nav a.router-link-exact-active {
  color: #f53e8a;
}
</style>
