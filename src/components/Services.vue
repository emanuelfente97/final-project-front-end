<template>
  <div class="container">
    <div class="details">
      <h1>Services</h1>
      <p class="cheat">We Offer the following services</p>
    </div>
    <div class="main-box">
      <div class="box box-red mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/CLjysMyq/pexels-photo-1319460.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Shears</h2>
        <hr />
        <p>
          ::before Lorem ipsum dolor, sit amet consectetur adipisicing elit.
          Assumenda labore. ::after
        </p>
      </div>

      <div class="box box-grey mx-auto">
        <img
          class="img"
          src="https://i.postimg.cc/C5VyVXqK/g40.jpg"
          style="width: 100px; height: 100px; border-radius: 50%"
        />

        <h2>Web Design</h2>
        <hr />
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda
          labore.
        </p>
      </div>

      <div class="box box-red mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/yWC3z1Vb/sc10.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Wash Hair</h2>
        <hr />
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda
          labore.
        </p>
      </div>

      <div class="box box-grey mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/7Yv5hn78/waxing.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Waxing</h2>
        <hr />
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda
          labore.
        </p>
      </div>
      <div class="box box-red mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/50hdYLvj/s30.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Web Design</h2>
        <hr />
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda
          labore.
        </p>
      </div>

      <div class="box box-grey mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/QMzvw1fS/services1.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Web Design</h2>
        <hr />
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Assumenda
          labore.
        </p>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
/* #243238
 #404044
 #D50000
*/

body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

.container {
  width: 80%;
  margin: 0 auto;
}

.details {
  text-align: center;
 
}
.cheat{
     margin-top: -75px;
}

.details h2 {
  color: #243238;
  font-size: 50px;
  margin: 0;
}
h1 {
  font-family: sans-serif;
  margin: 100px auto;
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

.main-box {
  display: flex;
  bottom: 100px;
  justify-content: center;
  flex-wrap: wrap;
}

.box {
  width: 300px;
  margin: 10px;
  text-align: center;
  padding: 40px 20px;
  color: #ffffff;
  position: relative;
  z-index: 2;
  border-radius: 5px;
}
.box > * {
  position: relative;
  z-index: 2;
  color: #ffffff;
}

.box::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  border: 2px solid rgba(255, 255, 255, 0.5);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
}

.box:hover::before {
  width: 95%;
  height: 95%;
  transition: all ease 0.5s;
}

.box .icon {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background-color: #ffffff;
  text-align: center;
  display: inline-block;
  position: relative;
}

.box .icon .fas {
  color: #404044;
  font-size: 30px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

hr {
  margin-top: 25px;
  margin-bottom: 25px;
  display: block;
  width: 70%;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.box a {
  text-decoration: none;
  color: #ffffff;
  text-transform: uppercase;
  background-color: #d50000;
  padding: 10px 25px;
  border-radius: 25px;
  margin-top: 25px;
  display: inline-block;
  font-weight: 600;
}
.box a:hover {
  background-color: #243238;
}

.box .white-border {
  border: 1px solid #ffffff;
}

.box-grey {
  background-color: #404044;
}

.box-red {
  background-color: #d50000;
}
.container{
  width: 80%;
}

</style>
