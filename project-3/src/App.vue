<template>
<div class='container'>
    <Navbar id="navbar"/>
    <Sidebar id="sidebar"/>
    <Main id="main"/>
    <Content1 id="content1"/>
    <Content2 id="content2"/>
    <Footer id="footer"/>
</div>


</template>

<script>
import Navbar from './components/Navbar.vue'
import Sidebar from './components/Sidebar.vue'
import Main from './components/Main.vue'
import Content1 from './components/Content1.vue'
import Content2 from './components/Content2.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Sidebar,
    Main,
    Content1,
    Content2,
    Footer,
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
  margin: 0;
  padding: 0;
}

:root {
  --main-radius: 5px;
  --main-padding: 5px;
}

.container {
  display: grid;
  height: 100vh;
  grid-template-columns: .5fr 1fr .5fr;
  grid-template-rows: .5fr 1fr 1fr .5fr;
  grid-template-areas: 
  "navbar navbar navbar"
  "sidebar main content1"
  "sidebar main content2"
  "footer footer footer";
  grid-gap: 0.2rem;
}

#navbar {
  background-color: green;
  grid-area: navbar;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#sidebar {
  background-color: green;
  grid-area: sidebar;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#main {
  background-color: green;
  grid-area: main;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#content1 {
  background-color: green;
  grid-area: content1;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#content2 {
  background-color: green;
  grid-area: content2;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#footer {
  background-color: green;
  grid-area: footer;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

@media only screen and (max-width: 650px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-rows: .25fr .25fr 1fr .5fr .5fr .5fr;
    grid-template-areas: 
    "navbar"
    "sidebar"
    "main"
    "content1"
    "content2"
    "footer";
  }
}

</style>
