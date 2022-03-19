<template>
  <Navbar @changePage="checkReservation" />
  <Home @myReservation="checkReservation" v-if="!reserve" />
  <About v-if="!reserve" />
  <Services v-if="!reserve" />
  <Prices v-if="!reserve" />
  <Team v-if="!reserve" />
  <Gallery v-if="!reserve" />
  
  <Contact v-if="!reserve" />
  <Reservation v-if="reserve" />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Home from "@/components/Home.vue";
import About from "@/components/About.vue";
import Services from "@/components/Services.vue";
import Prices from "@/components/prices.vue";
import Team from "@/components/Team.vue";

import Gallery from "@/components/gallery.vue";
import Contact from "@/components/contact.vue";
import Reservation from "@/components/Reservation.vue";

export default {
  components: {
    Navbar,
    Home,
    About,
    Services,
    Team,
    Prices,
    Gallery,
    Contact,
    Reservation,
  },
  data() {
    return {
      reserve: false,
    };
  },
  methods: {
    checkReservation: function (reserve) {
      console.log("we made it");
      this.reserve = reserve;
    },
  },
};
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
