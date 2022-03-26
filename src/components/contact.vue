<template>
  <section id="contact">
    <div class="contact-box">
      <div class="contact-links">
        <h2>Connect with us via our PR</h2>
        <div class="links">
          <div class="link">
            <link
              rel="stylesheet"
              href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
            />

            <body>
              <!-- <div class="hero"> -->
              <div class="social-links">
                <a
                  href="https://www.facebook.com/profile.php?id=100071966145885"
                  target="_blank"
                  ><i class="fab fa-facebook-f"></i
                ></a>
                <a
                  href="https://www.instagram.com/simthedikela/"
                  target="_blank"
                  ><i class="fab fa-instagram"></i
                ></a>
                <!-- <a href=""><i class="fab fa-twitter"></i></a> -->
                <!-- <a href="https://github.com/emanuelfente97"><i class="fab fa-github"></i></a> -->
                <a href="https://www.linkedin.com/in/ema97/" target="_blank"
                  ><i class="fab fa-linkedin-in"></i
                ></a>
              </div>
              <!-- </div> -->
            </body>
          </div>
        </div>
      </div>
      <div class="contact-form-wrapper">
        <form @submit.prevent="handleSubmit">
          <div class="form-item">
            <input v-model="name" type="text" name="name" required />
            <label>Name:</label>
          </div>
          <div class="form-item">
            <input v-model="email" type="email" name="email" required />
            <label>Email:</label>
          </div>
          <div class="form-item">
            <textarea
              v-model="message"
              id="message"
              class=""
              name="message"
              required
            ></textarea>
            <label>Message:</label>
          </div>
          <button class="submit-btn">Submit</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
  methods: {
    handleSubmit() {
      (this.name, this.email, this.message),
        fetch("https://final-project-backend-2022.herokuapp.com/api/contacts", {
          method: "POST",
          body: JSON.stringify({
            name: this.name,
            email: this.email,
            message: this.message,
            headers: { "Content-type": "application/json; charset=UTF-8" },
          }),
        })
          .then((response) => response.json())
          .then((json) => console.log(json.msg));
      alert("Sucesfully Sent").catch((err) => console.log(err.msg));
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

@import url("https://fonts.googleapis.com/css2?family=Arimo:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&display=swap");

* {
  margin: 0;
  box-sizing: border-box;
}

body {
  background-color: #6a9ac4;
}

#contact {
  background-color: #97aab9;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-box {
  width: clamp(100px, 90%, 1000px);
  margin: 80px 50px;
  display: flex;
  flex-wrap: wrap;
}

.contact-links,
.contact-form-wrapper {
  width: 50%;
  padding: 8% 5% 10% 5%;
}

.contact-links {
  background-color: #1a0819;
  background-image: url("https://i.postimg.cc/MKft6bpP/facials.jpg");
}

.contact-form-wrapper {
  background-color: #ffffff8f;
  border-radius: 0 10px 10px 0;
}

@media only screen and (max-width: 800px) {
  .contact-links,
  .contact-form-wrapper {
    width: 100%;
  }

  .contact-links {
    border-radius: 10px 10px 0 0;
  }

  .contact-form-wrapper {
    border-radius: 0 0 10px 10px;
  }
}

@media only screen and (max-width: 400px) {
  .contact-box {
    width: 95%;
    margin: 8% 5%;
  }
}

h2 {
  font-family: "Arimo", sans-serif;
  color: #fff;
  font-size: clamp(30px, 6vw, 60px);
  letter-spacing: 2px;
  text-align: center;
  transform: scale(0.95, 1);
}

.links {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-top: 50px;
}

.link {
  margin: 10px;
  cursor: pointer;
}

img {
  width: 45px;
  height: 45px;
  filter: hue-rotate(220deg) drop-shadow(2px 4px 4px #0006);
  transition: 0.2s;
  user-select: none;
}

img:hover {
  transform: scale(1.1, 1.1);
}

img:active {
  transform: scale(1.1, 1.1);
  filter: hue-rotate(220deg) drop-shadow(2px 4px 4px #222) sepia(0.3);
}

.form-item {
  position: relative;
}

label,
input,
textarea {
  font-family: "Poppins", sans-serif;
}

label {
  position: absolute;
  top: 10px;
  left: 2%;
  color: #999;
  font-size: clamp(14px, 1.5vw, 18px);
  pointer-events: none;
  user-select: none;
}

input,
textarea {
  width: 100%;
  outline: 0;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 20px;
  padding: 12px;
  font-size: clamp(15px, 1.5vw, 18px);
}

input:focus + label,
input:valid + label,
textarea:focus + label,
textarea:valid + label {
  font-size: clamp(13px, 1.3vw, 16px);
  color: #777;
  top: -20px;
  transition: all 0.225s ease;
}

.submit-btn {
  background-color: #fd917e;
  filter: drop-shadow(2px 2px 3px #0003);
  color: #fff;
  font-family: "Poppins", sans-serif;
  font-size: clamp(16px, 1.6vw, 18px);
  display: block;
  padding: 12px 20px;
  margin: 2px auto;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  user-select: none;
  transition: 0.2s;
}

.submit-btn:hover {
  transform: scale(1.1, 1.1);
}

.submit-btn:active {
  transform: scale(1.1, 1.1);
  filter: sepia(0.5);
}

@media only screen and (max-width: 800px) {
  h2 {
    font-size: clamp(40px, 10vw, 60px);
  }
}

@media only screen and (max-width: 400px) {
  h2 {
    font-size: clamp(30px, 12vw, 60px);
  }

  .links {
    padding-top: 30px;
  }

  img {
    width: 38px;
    height: 38px;
  }
}

@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap");

* {
  margin: 0;
  padding: 0;
  font-family: "Poppins", sans-serif;
}

.hero {
  width: 100%;
  height: 100vh;
  background: #f1f9ff;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}

h1 {
  font-size: 40px;
  margin-bottom: 100px;
  margin-top: -100px;
}

.social-links {
  display: flex;
}

.social-links a {
  width: 80px;
  height: 80px;
  text-align: center;
  text-decoration: none;
  color: #000;
  box-shadow: 0 0 20px 10px rgba(0, 0, 0, 0.05);
  margin: 0 30px;
  border-radius: 50%;
  position: relative;
  overflow: hidden;
  transition: transform 0.5s;
}

.social-links a .fab {
  font-size: 30px;
  line-height: 80px;
  position: relative;
  z-index: 10;
  transition: color 0.5s;
}

.social-links a::after {
  content: "";
  width: 100%;
  height: 100%;
  top: -90px;
  left: 0;
  background: #000;
  background: linear-gradient(-45deg, #ed1c94, #ffec17);
  position: absolute;
  transition: 0.5s;
}

.social-links a:hover::after {
  top: 0;
}

.social-links a:hover .fab {
  color: #fff;
}

.social-links a:hover {
  transform: translateY(-10px);
}
</style>
