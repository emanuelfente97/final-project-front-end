<template>
  <section id="home">
    <img
      class="home-img"
      src="data:image/webp;base64,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"
      alt=""
    />
    <div class="text-area">
      <!-- <h5 style="font-size: 2.25rem"><strong>Hello</strong></h5> -->
      <h3>
        <strong>You Imagine,We Create</strong><br />
        <strong>We are the best .</strong>
      </h3>

      <button
        type="button"
        class="btn btn-outline-primary"
        @click="makeReservation"
      >
        Make a reservation
      </button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      jwt: localStorage.getItem("jwt") || null,
    };
  },
  methods: {
    makeReservation: function () {
      if (localStorage.getItem("jwt") !== "undefined") {
        this.$emit("myReservation", true);
      } else {
        alert("you need to be logged in");
      }
    },
  },
};
</script>

<style scoped>
* {
  font-family: sans-serif;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

#home {
  background-image: linear-gradient(rgb(59 59 59 / 80%), rgb(107 106 106 / 10%)),
    url("https://i.postimg.cc/q7NQ1bJS/home3.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  height: 100vh;
  margin-top: -10vh;
}
.home-img {
  color: #fff;
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
.text-area {
  /* width: 90%; */
  font-size: 2.25rem;
  color: #fff;
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  /* position: fixed; */
}

@media screen and (max-width: 1024px) {
  .text-area {
    top: 55%;
    font-size: 2.25rem;
  }
}

.home-img {
  width: 40% !important;
}
.btn-outline-primary {
  border-color: #0db8de;
  color: #0db8de;
  border-radius: 0px;
  font-weight: bold;
  letter-spacing: 1px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
}
</style>
