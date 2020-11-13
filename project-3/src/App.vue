<template>
  <Menu/>
</template>

<script>
import Menu from './components/Menu.vue'

export default {
  name: 'App',
  components: {
    Menu
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@300&display=swap");
html {
  background: #08070f;
}

#app {
  font-family: "IBM Plex Sans", sans-serif;
  font-size: 1.4em;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: greenyellow;
  margin-top: 60px;
}
</style>
