<template>
  <section id="gallery" class="gallery">
    <h1 style="font-size: 45px"><strong> Our Gallery</strong></h1>
    <!-- <p>Find a range of sdjflhfouewhhwleifhilewyilygqieuhqiuhwelihqwwilehuilqweeiqw</p>
<p>ehilgeeukdgkuwgwdbhqwdukqdgku</p> -->

    <!-- <div class="container-all"> -->
    <div class="row" style="padding-top: 30px">
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/qMQGhTCn/g13.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/Qx4h6FTM/g2.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/RFpqwg4M/g4.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
    </div>

    <div class="row">
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/RFpqwg4M/g4.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/SRN9LnBh/g20.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
      <div class="col-sm-12 col-md-4">
        <img src="https://i.postimg.cc/FKMk6PwD/g6.jpg" alt="" />
        <span class="title">Lorem ipsum dolor</span>
        <span class="text"
          >Morbi diam viverra mattis sociis magna, habitasse penatibus non
          lectus</span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Poppins");
body,
html {
  margin: 0;
  background: #2b2927;
  font-family: "Poppins", sans-serif;
}

h1 {
  text-align: center;
  color: #2c3e50;
}
.gallery {
  background: #fff;
  padding-top: 70px;
  padding-bottom: 30px;
}
.container-all {
  width: fit-content;
  margin: 10px auto;
  height: 80vh;
  background: black;
}
p {
  color: green;
}
.container {
  width: calc(33% - 6px);
  overflow: hidden;
  height: fit-content;
  margin: 3px;
  padding: 0;
  display: block;
  position: relative;
  float: left;
}
.row {
  width: 100%;
}
img {
  width: 100%;
  transition-duration: 0.3s;
  max-width: 100%;
  display: block;
  overflow: hidden;
  cursor: pointer;
}
.title {
  position: absolute;
  display: block;
  cursor: pointer;
  top: 35%;
  display: none;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
  font-weight: bold;
  font-size: 1.6em;
  text-shadow: 1px 5px 10px black;
  transition-duration: 0.3s;
}
.text {
  position: absolute;
  top: 70%;
  cursor: pointer;
  max-width: 80%;
  text-align: center;
  left: 50%;
  text-shadow: 1px 5px 10px black;
  font-size: 1em;
  display: none;
  margin-right: -50%;
  transition-duration: 0.3s;
  transform: translate(-50%, -50%);
}
.container:hover img {
  transform: scale(1.2);
  transition-duration: 0.3s;
  filter: grayscale(50%);
  opacity: 0.7;
}
.container:hover span {
  color: white;
  display: block;
  transition-duration: 0.3s;
}
@media only screen and (max-width: 900px) {
  .container {
    width: calc(50% - 6px);
  }
}
@media only screen and (max-width: 400px) {
  .container {
    width: 80%;
  }
}

@media screen and (max-width: 925px) {
  .container-all {
    height: 100vh !important;
  }
}
</style>
