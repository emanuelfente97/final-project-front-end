<template>
  <Navbar @changePage="checkReservation" @changedLoginState="changedState" />
  <Home @myReservation="checkReservation" v-if="!reserve" />
  <About v-if="!reserve" />
  <Services v-if="!reserve" :key="key" />

  <Team v-if="!reserve" />
  <Gallery v-if="!reserve" />
  <Contact v-if="!reserve" />
  <Footer v-if="!reserve" />

  <Reservation v-if="reserve" />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Home from "@/components/Home.vue";
import About from "@/components/About.vue";
import Services from "@/components/Services.vue";

import Team from "@/components/Team.vue";

import Gallery from "@/components/gallery.vue";
import Contact from "@/components/contact.vue";
import Reservation from "@/components/Reservation.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    Navbar,
    Home,
    About,
    Services,
    Team,

    Gallery,
    Contact,
    Reservation,
    Footer,
  },
  data() {
    return {
      reserve: false,
      key: 0,
    };
  },
  methods: {
    checkReservation: function (reserve) {
      this.reserve = reserve;
    },
    changedState() {
      this.key++;
    },
  },
};
</script>

<style>
.modal-backdrop.show {
  z-index: 1 !important;
}
.modal-backdrop {
  z-index: 1 !important;
}
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
