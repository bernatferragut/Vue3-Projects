<template>
<div>
    <Top/>
    <Search/>
    <Hodl/>
    <Greed/>
    <Pie/>
    <Footer/>
</div>


</template>

<script>
import Top from './components/Top.vue'
import Search from './components/Search.vue'
import Hodl from './components/Hodl.vue'
import Greed from './components/Greed.vue'
import Pie from './components/Pie.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Top,
    Search,
    Hodl,
    Greed,
    Pie,
    Footer
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
