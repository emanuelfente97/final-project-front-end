<template>
  <Navbar />
  <Home />
  <About />
  <Services />
   <Team />
   <gallery/>
   <prices />
  <Contact />
  <router-view/>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Home from "./components/Home.vue"
import About from "./components/About.vue"
import Services from "./components/Services.vue"
import Team from "./components/Team.vue"
import prices from "./components/prices.vue"
import gallery from "./components/gallery.vue"
import Contact from "./components/contact.vue"


export default {
  components: {
    Navbar,
    Home,
    About,
    Services,
    Team,
    prices,
    gallery,
    Contact
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
  background: black;
  height: 100vh;
}
</style>
