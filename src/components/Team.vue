<template>
  <section id="team" class="section-team">
    <div class="container">
      <div class="container">
        <div class="row justify-content-center text-center">
          <div class="col-md-8 col-lg-6">
            <div class="header-section">
              <h2 class="title">Meet our Team members</h2>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-6 col-lg-4 col-xl-3">
            <div class="single-person">
              <div class="person-image">
                <img src="https://i.postimg.cc/7LyHsBRk/T1.jpg" alt="" />
              </div>
              <div class="person-info">
                <h3 class="full-name">Lumko Mda</h3>
                <span class="speciality">Specialist</span>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-lg-4 col-xl-3">
            <div class="single-person">
              <div class="person-image">
                <img src="https://i.postimg.cc/yYHXXB16/t.jpg" alt="" />
              </div>
              <div class="person-info">
                <h3 class="full-name">Emanuel Adams</h3>
                <span class="speciality">Public Relations</span>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-lg-4 col-xl-3">
            <div class="single-person">
              <div class="person-image">
                <img src="https://i.postimg.cc/NGVwCJyz/t3.jpg" alt="" />
              </div>
              <div class="person-info">
                <h3 class="full-name">David Specks</h3>
                <span class="speciality">Hair cuts </span>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-lg-4 col-xl-3">
            <div class="single-person">
              <div class="person-image">
                <img src="https://i.postimg.cc/ht7DDFmx/t23.jpg" alt="" />
              </div>
              <div class="person-info">
                <h3 class="full-name">Johnson Daniels</h3>
                <span class="speciality">Hair Cuts </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
p,
a,
h1,
h2,
h3,
h4 {
  margin: 0;
  padding: 0;
}

.section-team {
  font-family: "Poppins", sans-serif;
  padding: 80px 0;
  background: #c9d0d3;
}

.section-team .header-section {
  margin-bottom: 50px;
}

.section-team .header-section .small-title {
  margin-bottom: 25px;
  font-size: 16px;
  font-weight: 500;
  color: #3e64ff;
}

.section-team .header-section .title {
  font-weight: 700;
  font-size: 45px;
}

.section-team .single-person {
  margin-top: 30px;
  padding: 30px;
  background-color: #f6f9ff;
  border-radius: 5px;
}

.section-team .single-person:hover {
  background: linear-gradient(to right, #016cec, #00b5f7);
}

.section-team .single-person .person-image {
  position: relative;
  margin-bottom: 50px;
  border-radius: 50%;
  border: 4px dashed transparent;
  transition: padding 0.3s;
}

.section-team .single-person:hover .person-image {
  padding: 12px;
  border: 4px dashed #fff;
}

.section-team .single-person .person-image img {
  width: 100%;
  border-radius: 50%;
}

.section-team .single-person .person-image .icon {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translate(-50%, 50%);
  display: inline-block;
  width: 60px;
  height: 60px;
  line-height: 60px;
  text-align: center;
  background: linear-gradient(to right, #016cec, #00b5f7);
  color: #fff;
  border-radius: 50%;
  font-size: 24px;
}

.section-team .single-person:hover .person-image .icon {
  background: none;
  background-color: #fff;
  color: #016cec;
}

.section-team .single-person .person-info .full-name {
  margin-bottom: 10px;
  font-size: 28px;
  font-weight: 700;
}

.section-team .single-person .person-info .speciality {
  text-transform: uppercase;
  font-size: 14px;
  color: #016cec;
}

.section-team .single-person:hover .full-name,
.section-team .single-person:hover .speciality {
  color: #fff;
}
</style>
