<template>
<section id="prices" class="price">
  <h1>Prices</h1>
  <p> Below find more about our affordable prices</p>
  <div class = "container">
  <div class="container" style="margin-top:30px">
    <div class="row">
      <div class="col-sm-12 col-md-6 col-lg-4">
        <div class="card mx-auto" style="width: 100%; column-gap:20px">
          <img
            src="https://i.postimg.cc/CLjysMyq/pexels-photo-1319460.jpg"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">Special Treats</h5>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Customized Designs</li>
            <li class="list-group-item">Aefro Styles</li>
            <li class="list-group-item">Braiding: R300</li>
          </ul>
          <div class="card-body">
            <button
              style="margin-right: 30px"
              type="button"
              class="btn btn-secondary"
            >
            R120
            </button>
            <button
              style="margin-left: 30px"
              type="button"
              class="btn btn-secondary"
            >
              Book
            </button>
          </div>
        </div>
      </div>


      <div class="col-sm-12  col-md-6  col-lg-4">
        <div class="card mx-auto" style="width: 100%; column-gap:20px">
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
              style="margin-right: 30px"
              type="button"
              class="btn btn-secondary"
            >
              R120
            </button>
            <button
              style="margin-left: 30px"
              type="button"
              class="btn btn-secondary"
            >
              Book
            </button>
          </div>
        </div>
      </div>


      <div class="col-sm-12 col-md-6 col-lg-4">
       
        <div class="card mx-auto" style="width: 100%; column-gap:50px">
          <img
            src="https://i.postimg.cc/CLjysMyq/pexels-photo-1319460.jpg"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">Hair Cuts</h5>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">Normal Cuts :R70</li>
            <li class="list-group-item">Triming : R50</li>
            <li class="list-group-item">Waxing : R45</li>
          </ul>
          <div class="card-body">
            <button type="button" class="btn btn-secondary"> R195</button>&nbsp;
            &nbsp;
            <button type="button" class="btn btn-secondary">Book</button>
          </div>
        </div>
      </div>
        </div>
      </div>
    </div>
  
</section>
</template>

<script></script>

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

.container{
gap: 30px;
}
.card{
  width:300px
}
</style>
