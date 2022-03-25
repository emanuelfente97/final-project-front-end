<template>
  <!-- <section class="header" id="navbar">    -->
  <nav class="navbar navbar-expand-lg fixed-top">
    <img src="https://i.postimg.cc/1XXDDgFq/logo5.jpg" class="logo" />

    <button
      class="navbar-toggler ms-auto"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        x="0px"
        y="0px"
        width="24"
        height="24"
        viewBox="0 0 172 172"
        style="fill: #000000"
      >
        <g
          fill="none"
          fill-rule="nonzero"
          stroke="none"
          stroke-width="1"
          stroke-linecap="butt"
          stroke-linejoin="miter"
          stroke-miterlimit="10"
          stroke-dasharray=""
          stroke-dashoffset="0"
          font-family="none"
          font-weight="none"
          font-size="none"
          text-anchor="none"
          style="mix-blend-mode: normal"
        >
          <path d="M0,172v-172h172v172z" fill="none"></path>
          <g fill="#ffffff">
            <path
              d="M14.33333,35.83333v14.33333h143.33333v-14.33333zM14.33333,78.83333v14.33333h143.33333v-14.33333zM14.33333,121.83333v14.33333h143.33333v-14.33333z"
            ></path>
          </g>
        </g>
      </svg>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mx-auto">
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#home"
            >Home</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#about"
            >About</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#services"
            >Services</a
          >
        </li>
        <li class="nav-item">
          <a  class="nav-link" href="#prices"
            >Prices
          </a>
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#gallery"
            ><i class="bi bi-file-earmark-code-fill"></i> Gallery</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#team"
            > Team</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#contact"
            >Contacts</a
          >
        </li>
        <div class="but">
          &nbsp; &nbsp;
          <!-- Button trigger modal -->
          <button
            type="button"
            class="btn btn-outline-primary"
            data-bs-toggle="modal"
            data-bs-target="#exampleModal"
          >
            Sign in
          </button>

          <!-- Modal -->
          <div
            class="modal fade"
            id="exampleModal"
            tabindex="-1"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
          >
            <div
              class="modal-dialog"
              style="
                padding-top: 100px;
                padding-bottom: auto;
                height: 400px;
                margin-bottom: 100px;
              "
            >
              <div class="modal-content">
                <div class="modal-header" style="height: 20px">
                  <h5 class="modal-title" id="exampleModalLabel">
                    Modal title
                  </h5>
                  <button
                    type="button"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </div>
                <div class="modal-body">
                  <div class="container">
                    <div class="row">
                      <div class="col-lg-3 col-md-2"></div>
                      <div class="col-lg-6 col-md-8 login-box">
                        <div class="col-lg-12 login-key">
                          <i class="fa fa-key" aria-hidden="true"></i>
                        </div>
                        <div class="col-lg-12 login-title">Log-in Form</div>

                        <div class="col-lg-12 login-form">
                          <div class="col-lg-12 login-form">
                            <form @submit.prevent="login">
                              <div class="form-group">
                                <label class="form-control-label"
                                  >USERNAME</label
                                >
                                <input
                                  type="text"
                                  v-model="username"
                                  required
                                  class="form-control"
                                />
                              </div>
                              <div class="form-group">
                                <label class="form-control-label"
                                  >PASSWORD</label
                                >
                                <input
                                  v-model="password"
                                  type="password"
                                  required
                                  class="form-control"
                                  i
                                />
                              </div>

                              <div class="col-lg-12 loginbttm">
                                <div class="col-lg-6 login-btm login-text">
                                  <!-- Error Message -->
                                </div>
                                <div class="col-lg-6 login-btm login-button">
                                  <button
                                    type="submit"
                                    class="btn btn-outline-primary"
                                  >
                                    LOGIN
                                  </button>
                                  <button
                                    type="button"
                                    class="btn btn-outline-secondary"
                                    data-bs-toggle="modal"
                                    data-bs-target="#exampleModal1"
                                  >
                                    Sign up
                                  </button>

                                  <!-- <button type="submit" class="btn btn-outine-secondary">Sign up</button> -->
                                </div>
                              </div>
                            </form>
                          </div>
                        </div>
                        <div class="col-lg-3 col-md-2"></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Modal for sigup -->
          <div
            class="modal fade"
            id="exampleModal1"
            tabindex="-1"
            aria-labelledby="exampleModalLabel1"
            aria-hidden="true"
          >
            <div
              class="modal-dialog"
              style="
                padding-top: 100px;
                padding-bottom: auto;
                height: 400px;
                margin-bottom: 100px;
              "
            >
              <div class="modal-content">
                <div class="modal-header" style="height: 20px">
                  <h5 class="modal-title" id="exampleModalLabel1">
                    Modal title
                  </h5>
                  <button
                    type="button"
                    class="btn-close"
                    data-bs-dismiss="modal"
                    aria-label="Close"
                  ></button>
                </div>
                <div class="modal-body">
                  <div class="container">
                    <div class="row">
                      <div class="col-lg-3 col-md-2"></div>
                      <div class="col-lg-6 col-md-8 login-box">
                        <div class="col-lg-12 login-key">
                          <i class="fa fa-key" aria-hidden="true"></i>
                        </div>
                        <div class="col-lg-12 login-title">Sign-up Form</div>

                        <div class="col-lg-12 login-form">
                          <div class="col-lg-12 login-form">
                            <form @submit.prevent="register">
                              <div class="form-group">
                                <label class="form-control-label"
                                  >USERNAME</label
                                >
                                <input
                                  type="text"
                                  v-model="username"
                                  required
                                  class="form-control"
                                />
                              </div>
                              <div class="form-group">
                                <label class="form-control-label">Email</label>
                                <input
                                  type="email"
                                  v-model="email"
                                  required
                                  class="form-control"
                                />
                              </div>
                              <div class="form-group">
                                <label class="form-control-label"
                                  >PASSWORD</label
                                >
                                <input
                                  v-model="password"
                                  type="password"
                                  required
                                  class="form-control"
                                  i
                                />
                              </div>

                              <div class="col-lg-12 loginbttm">
                                <div class="col-lg-6 login-btm login-text">
                                  <!-- Error Message -->
                                </div>
                                <div class="col-lg-6 login-btm login-button">
                                  <button
                                    type="submit"
                                    class="btn btn-outline-primary"
                                  >
                                    Sign up
                                  </button>
                                </div>
                              </div>
                            </form>
                          </div>
                        </div>
                        <div class="col-lg-3 col-md-2"></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <button @click="logout" type="button" class="btn btn-outline-primary">
            Log out
          </button>
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    hideReservation: function () {
      this.$emit("changePage", false);
    },
  },
  data() {
    return {
      username: "",
      password: "",
      email: "",
    };
  },
  methods: {
    login() {
      fetch("https://final-project-backend-2022.herokuapp.com/api/auth/login", {
        method: "POST",
        body: JSON.stringify({
          username: this.username,
          password: this.password,
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      })
        .then((response) => response.json())
        .then(async(json) => {
          if(json.accessToken)
          console.log(json);
          console.log(json.accessToken)
          alert("User logged in");
          await localStorage.setItem("jwt", json.accessToken);
          
        })
        .catch((err) => {
          alert(err);
        });
    },
    logout() {
      localStorage.clear();
      console.log("logout");
      alert("user logged out");
    },
    register() {
      fetch(" https://final-project-backend-2022.herokuapp.com/api/auth/register", {
        method: "POST",
        body: JSON.stringify({
          username: this.username,
          password: this.password,
          email: this.email,
        }),
        mode: "cors",
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      })
        .then((response) => response.json())
        .then((json) => {
          // console.log(json);
          localStorage.getItem("jwt", json.accessToken);
          console.log(json.accessToken)
          alert("User signed up");
          // this.$router.push({ name: "services" });
        })
        .catch((err) => {
          alert(err);
        });
    },
  },
};
</script>

<style scoped>
.logo {
  width: 100px;
  position: relative;
  top: 2%;
  left: 10%;
  width: 60px;
  height: 60px;
}

.navbar {
  display: flex;

  justify-content: space-between;
  align-items: center;
  background-color: black;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;

  z-index: 99999999999999999999999;
  box-shadow: 0 4px 12px 0 #fbfbfb33, 0 2px 4px rgb(0 0 0 / 5%);
}

.navbar {
  flex: 1;
  text-align: center;
  color: white;
}
.nav-cont ul li {
  list-style: none;
  display: inline-block;
  padding: 8px 12px;
  position: relative;
  color: #a3aab0;
}
.navbar ul li a {
  color: #ffff;
  text-decoration: none;
  font-size: 15px;
}
.navbar ul li::after {
  content: "";
  width: 0%;
  height: 2px;
  background: red;
  display: block;
  /* margin: auto; */
  transition: 0.5s;
}

.navbar ul li:hover::after {
  width: 100%;
  color: white;
}
@media screen and (min-width: 992px) {
  .but {
    position: relative;
    left: 10%;
  }
}

body {
  background: #222d32;
  font-family: "Roboto", sans-serif;
}

.login-box {
  margin-top: 0px;
  height: 100%;
  width: 100%;
  height: auto;
  background: #1a2226;
  text-align: center;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
}

.login-key {
  height: 100px;
  font-size: 80px;
  line-height: 100px;
  background: -webkit-linear-gradient(#27ef9f, #0db8de);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.login-title {
  margin-top: 15px;
  text-align: center;
  font-size: 30px;
  letter-spacing: 2px;
  margin-top: 15px;
  font-weight: bold;
  color: #ecf0f5;
}

.login-form {
  margin-top: 25px;
  text-align: left;
}

input[type="text"] {
  background-color: #1a2226;
  border: none;
  border-bottom: 2px solid #0db8de;
  border-top: 0px;
  border-radius: 0px;
  font-weight: bold;
  outline: 0;
  margin-bottom: 20px;
  padding-left: 0px;
  color: #ecf0f5;
}

input[type="password"] {
  background-color: #1a2226;
  border: none;
  border-bottom: 2px solid #0db8de;
  border-top: 0px;
  border-radius: 0px;
  font-weight: bold;
  outline: 0;
  padding-left: 0px;
  margin-bottom: 20px;
  color: #ecf0f5;
}

.form-group {
  outline: 0px;
}

.form-control:focus {
  border-color: inherit;
  -webkit-box-shadow: none;
  box-shadow: none;
  border-bottom: 2px solid #0db8de;
  outline: 0;
  background-color: #1a2226;
  color: #ecf0f5;
}

input:focus {
  outline: none;
  box-shadow: 0 0 0;
}

label {
  margin-bottom: 0px;
}

.form-control-label {
  font-size: 10px;
  color: #6c6c6c;
  font-weight: bold;
  letter-spacing: 1px;
}

.btn-outline-primary {
  border-color: #0db8de;
  color: #0db8de;
  border-radius: 0px;
  font-weight: bold;
  letter-spacing: 1px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
}

.btn-outline-primary:hover {
  background-color: #0db8de;
  right: 0px;
}

.login-btm {
  float: left;
}

.login-button {
  /* padding-right: 0px; */
  /* text-align: right; */
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 25px;
}

.login-text {
  text-align: left;
  padding-left: 0px;
  color: #a2a4a4;
}
.login-Email {
  text-align: left;
  padding-left: 0px;
  color: #a2a4a4;
}
.loginbttm {
  padding: 0px;
}
</style>
