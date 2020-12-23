<template>
  <div class='container'>
    <Title id="title"/>
    <Search id="search"/>
    <Total id="total"/>
    <Content1 id="content1"/>
    <Main id="main"/>
    <suspense>
        <Content2 id="content2"/>
    </suspense>
    <Footer id="footer"/>
  </div>
</template>

<script>
import Title from './components/Title.vue'
import Search from './components/Search.vue'
import Total from './components/Total.vue'
import Content1 from './components/Content1.vue'
import Main from './components/Main.vue'
import Content2 from './components/Content2.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Title,
    Search,
    Total,
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
  color: black ;
  margin: 0;
  padding: 0;
}

:root {
  --main-radius: 5px;
  --main-padding: 5px;
  --main-bgcolor: greenyellow;
}

.container {
  display: grid;
  height: 100vh;
  grid-template-columns: .5fr 1fr .5fr;
  grid-template-rows: .5fr 1fr 1fr .5fr;
  grid-template-areas: 
  "title search total"
  "content1 main content2"
  "content1 main content2"
  "footer footer footer";
  grid-gap: 0.2rem;
}

#title {
  background-color: var(--main-bgcolor);
  grid-area: title;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#search { 
  background-color: var(--main-bgcolor);
  grid-area: search;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#total {
  background-color: var(--main-bgcolor);
  grid-area: total;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#main {
  background-color: var(--main-bgcolor);
  grid-area: main;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#content1 {
  background-color: var(--main-bgcolor);
  grid-area: content1;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#content2 {
  background-color: var(--main-bgcolor);
  grid-area: content2;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

#footer {
  background-color: var(--main-bgcolor);
  grid-area: footer;
  border-radius: var(--main-radius);
  padding-top: var(--main-radius);
}

@media only screen and (max-width: 650px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-rows: .25fr .25fr 1fr .5fr .5fr .5fr;
    grid-template-areas: 
    "title"
    "search"
    "main"
    "total"
    "content1"
    "content2"
    "footer";
  }
}

</style>
