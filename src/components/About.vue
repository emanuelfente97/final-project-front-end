<template>
  <section class="section about-section gray-bg" id="about">
    <h3 class="title"><span id="title">About us</span></h3>
    <div class="container">
      <div class="row align-items-center flex-row-reverse">
        <div class="col-lg-6">
          <div class="about-text data-aos=fade-right">
            <h6 style="color: purple; font-size: 25px">Legend's Barber Shop</h6>
            <p>
              <strong
                ><span style="color: purple">Legends barber shop,</span></strong
              >
              prides it self for delivering the best service in town. we believe
              that going to a barber shop should not only be about doing an
              errand but an expirience. We prioritise our customers, by making
              sure that all they do is tell us what they want and we will
              visulaise and create. Ours is to be creative and deliver their
              wishes. We are art fanatics and we create that through cutting
              hair.We are committed to being an inclusive and welcoming
              environment for every client and member of our team who enter our
              space regardless of gender, race, sexual orientation, religion or
              politics. To find more about
              <span style="color: purple">Legends Barber Shop</span>
              click on the buttons below:
            </p>
            <div class="row about-list">
              <div class="col-md-6">
                <div class="media">
                  <a href="#services"
                    ><button type="button" class="btn btn-primary">
                      Services
                    </button></a
                  >
                </div>
              </div>
              <div class="col-lg-6">
                <div class="media">
                  <a href="#contact">
                    <button type="button" class="btn btn-primary">
                      Contact us
                    </button></a
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="about-pic data-aos=fade-left">
            <img
              class="responsive profile"
              src="https://i.postimg.cc/qq5kjGdC/about-removebg-preview.png"
              title=""
              alt=""
              style="width: 80%; height: 50%"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script></script>
<style scoped>
.section {
  /* padding: 60px; */
  background-color: #c9d0d3;
}
#about {
  padding-top: 70px;
}
.title {
  text-align: center;
  justify-content: center;
  position: relative;
  display: inline-block;
  border-bottom-width: 5px;
  font-size: 45px;
  width: 100%;
  height: 50px;
  margin: 0 0 6px;
  font-weight: 700;
}
h3 {
  padding-bottom: 30px;
}

.about-text {
  padding-top: 20px;
}
* {
  text-align: start;
}
@media (max-width: 767px) {
  .about-text h3 {
    font-size: 35px;
  }
}
.about-text h6 {
  font-weight: 600;
  margin-bottom: 15px;
}
@media (max-width: 767px) {
  .about-text h6 {
    font-size: 18px;
  }
}
.about-text p {
  font-size: 18px;
  max-width: 450px;
  text-align: justify;
}
.about-text p mark {
  font-weight: 600;
  color: #20247b;
}
.about-list {
  padding-top: 10px;
}
.about-list .media {
  padding: 5px 0;
}
.about-list label {
  color: #20247b;
  font-weight: 600;
  width: 88px;
  margin: 0;
  position: relative;
}
.about-list label:after {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  right: 11px;
  width: 1px;
  height: 12px;
  background: #20247b;
  -moz-transform: rotate(15deg);
  -o-transform: rotate(15deg);
  -ms-transform: rotate(15deg);
  -webkit-transform: rotate(15deg);
  transform: rotate(15deg);
  margin: auto;
  opacity: 0.5;
}
.about-list p {
  margin: 0;
  font-size: 15px;
}
@media (max-width: 991px) {
  .about-pic {
    margin-top: -160px;
  }
}
.about-section .counter {
  padding: 22px 20px;
  background: #ffffff;
  border-radius: 10px;
  box-shadow: 0 0 30px rgba(31, 45, 61, 0.125);
}
.about-section .counter .count-data {
  margin-top: 10px;
  margin-bottom: 10px;
}
.about-section .counter .count {
  font-weight: 700;
  color: #20247b;
  margin: 0 0 5px;
}
.about-section .counter p {
  font-weight: 600;
  margin: 0;
}
mark {
  background-image: linear-gradient(
    rgba(252, 83, 86, 0.6),
    rgba(252, 83, 86, 0.6)
  );
  background-size: 100% 3px;
  background-repeat: no-repeat;
  background-position: 0 bottom;
  background-color: transparent;
  padding: 0;
  color: currentColor;
}
.theme-color {
  color: #fc5356;
}
.dark-color {
  color: #20247b;
}
</style>
