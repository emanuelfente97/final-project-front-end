<template>
  <Navbar />
  <Home />
  <About />
  <Services />
   <Team />
  <contact />
  
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Home from "./components/Home.vue"
import About from "./components/About.vue"
import Services from "./components/Services.vue"
import Team from "./components/Team.vue"
import contact from "./components/contact.vue"


export default {
  components: {
    Navbar,
    Home,
    About,
    Services,
    Team,
    contact
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
