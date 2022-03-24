<template>
<section id="prices" class="price">
  <h1>Prices</h1>
  <p> Below find more about our affordable prices</p>
  <div class="container">
  <div class = "container">
  <div class="container" style="margin-top:20px">
    <div class="row" >
      <div class="col-sm-12 col-md-6 col-lg-4 ">
        <div class="card">
          <img
            src="https://i.postimg.cc/YqX0qKSq/pexels-photo-995300.jpg"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">Special Treats</h5>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Customized Designs</li>
            <li class="list-group-item">Aefro Styles</li>
            <li class="list-group-item">Waxing : R45</li>
          </ul>
          <div class="card-body">
          
            <button
            @click="makeReservation"
              type="button"
              class="btn btn-secondary"
            >
              Make A Reservation
            </button>
          </div>
        </div>
      </div>


      <div class="col-sm-12  col-md-6  col-lg-4">
        <div class="card" >
          <img
            src="https://i.postimg.cc/CLjysMyq/pexels-photo-1319460.jpg"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">Other Services</h5>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Hair Coloring: R150</li>
            <li class="list-group-item">Grey Blending: R130</li>
            <li class="list-group-item">Facials : R65</li>
          </ul>
          <div class="card-body">
           
            <button
           @click="makeReservation"
              type="button"
              class="btn btn-secondary"
            >
               Make A Reservation
            </button>
          </div>
        </div>
      </div>


      <div class="col-sm-12 col-md-6 col-lg-4 ">
       
        <div class="card" >
          <img
            src="https://i.postimg.cc/Fs9yf4gM/pexels-photo-4449790.jpg"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">Hair Cuts</h5>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Normal Cuts :R70</li>
            <li class="list-group-item">Triming : R50</li>
            <li class="list-group-item">Faders: R100</li>
          </ul>
          <div class="card-body">
            <!-- <button type="button" class="btn btn-secondary"> R195</button>&nbsp; -->
          
            <button @click="makeReservation" type="button" class="btn btn-secondary">Make a Reservation</button>
          </div>
        </div>
      </div>
        </div>
  </div>
      </div>
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
.price{
padding-top: 60px ;
background: grey;
}

h1 {
  font-family: sans-serif;
  margin: 30px auto;
  color: #228b22;
  text-align: center;
  font-size: 30px;
  max-width: 420px;
  position: relative;
}
.bt{
  margin-left:auto;
  margin-right:auto
}

h1:before {
  content: "";
  display: block;
  width: 120px;
  height: 2px;
  background: #000;
  left: 0;
  top: 50%;
  position: absolute;
}
h1:after {
  content: "";
  display: block;
  width: 120px;
  height: 2px;
  background: #000;
  right: 0;
  top: 50%;
  position: absolute;
}

/* .container{
gap: 30px;
} */
.row {
  width: 95%;
  margin-inline: auto;
}
.card{
  width:300px;
  margin:10px;
  height:500px;
  position: relative;
  /* column-gap: 10px */

}
</style>
