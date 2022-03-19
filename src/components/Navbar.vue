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
          <a class="nav-link" aria-current="page" href="#navbar"
            ><i class="fa fa-fw fa-home"></i>Home</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#about"><i class="fa fa-user"></i> About</a>
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#services"
            ><i class="fa fa-bars"></i> Services</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#prices"
            ><i class="bi bi-pencil-square"></i>Prices
          </a>
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#gallery"
            ><i class="bi bi-file-earmark-code-fill"></i> Gallery</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#Team"
            ><i class="bi bi-people-fill"></i> Team</a
          >
        </li>
        <li class="nav-item">
          <a @click="hideReservation" class="nav-link" href="#contact"
            ><i class="fa fa-fw fa-envelope"></i>Contacts</a
          >
        </li>
        <div class="but">
          &nbsp; &nbsp;
          <!-- Button trigger modal -->
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-toggle="modal"
            data-bs-target="#exampleModal1"
          >
            Sign up / sign in
          </button>

          <!-- Modal -->
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
                  <div class="login-wrap">
                    <div class="login-html">
                      <input
                        id="tab-1"
                        type="radio"
                        name="tab"
                        class="sign-in"
                        checked
                      /><label for="tab-1" class="tab">Sign In</label>
                      <input
                        id="tab-2"
                        type="radio"
                        name="tab"
                        class="sign-up"
                      /><label for="tab-2" class="tab">Sign Up</label>
                      <div class="login-form">
                        <div class="sign-in-htm">
                          <div class="group">
                            <label for="user" class="label">Username</label>
                            <input id="user" type="text" class="input" />
                          </div>
                          <div class="group">
                            <label for="pass" class="label">Password</label>
                            <input
                              id="pass"
                              type="password"
                              class="input"
                              data-type="password"
                            />
                          </div>
                          <div class="group">
                            <input
                              id="check"
                              type="checkbox"
                              class="check"
                              checked
                            />
                            <label for="check"
                              ><span class="icon"></span> Keep me signed
                              in</label
                            >
                          </div>
                          <div class="group">
                            <input
                              type="submit"
                              class="button"
                              value="Sign In"
                            />
                          </div>
                        </div>
                        <div class="sign-up-htm">
                          <div class="group">
                            <label for="user" class="label">Username</label>
                            <input id="user" type="text" class="input" />
                          </div>
                          <div class="group">
                            <label for="pass" class="label">Password</label>
                            <input
                              id="pass"
                              type="password"
                              class="input"
                              data-type="password"
                            />
                          </div>

                          <div class="group">
                            <label for="pass" class="label"
                              >Email Address</label
                            >
                            <input id="pass" type="text" class="input" />
                          </div>
                          <div class="group">
                            <input
                              type="submit"
                              class="button"
                              value="Sign Up"
                            />
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    hideReservation: function (){
      this.$emit("changePage", false)
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
/* .but {
  position: relative;
  left: 10%;
} */

.navbar {
  display: flex;
  /* padding: 1% 4%; */
  justify-content: space-between;
  align-items: center;
  background-color: black;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  /* height:20px !important; */
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
  align-items: center;
  background-color: #000;
  display: flex;
  justify-content: center;
  height: 100vh;
}

.form {
  background-color: #15172b;
  border-radius: 20px;
  box-sizing: border-box;
  height: 500px;
  padding: 20px;
  width: 320px;
  margin-left: auto;
  margin-right: auto;
}

.title {
  color: #eee;
  font-family: sans-serif;
  font-size: 36px;
  font-weight: 600;
  margin-top: 30px;
}

.subtitle {
  color: #eee;
  font-family: sans-serif;
  font-size: 16px;
  font-weight: 600;
  margin-top: 10px;
}

.input-container {
  height: 50px;
  position: relative;
  width: 100%;
}

.ic1 {
  margin-top: 40px;
}

.ic2 {
  margin-top: 30px;
}

.input {
  background-color: #303245;
  border-radius: 12px;
  border: 0;
  box-sizing: border-box;
  color: #eee;
  font-size: 18px;
  height: 100%;
  outline: 0;
  padding: 4px 20px 0;
  width: 100%;
}


.placeholder {
  color: none !important;
  font-family: sans-serif;
  left: 20px;
  line-height: 14px;
  pointer-events: none;
  position: absolute;
  transform-origin: 0 50%;
  transition: transform 200ms, color 200ms;
  top: 20px;
}
/* 
.input:focus ~ .placeholder,
.input:not(:placeholder-shown) ~ .placeholder {
  transform: translateY(-30px) translateX(10px) scale(0.75);
} */

/* .input:not(:placeholder-shown) ~ .placeholder {
  color: #808097;
} */
/* 
.input:focus ~ .placeholder {
  color: #dc2f55;
} */

.submit {
  background-color: #08d;
  border-radius: 12px;
  border: 0;
  box-sizing: border-box;
  color: #eee;
  cursor: pointer;
  font-size: 18px;
  height: 50px;
  margin-top: 38px;

  text-align: center;
  width: 100%;
}
.close {
  opacity: 10;
  margin-left: auto;
  margin-right: auto;
}

.submit:active {
  background-color: #06b;
}
html {
  height: 100%;
}
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  background: linear-gradient(#141e30, #04080e);
}

.login-box {
  /* position: absolute; */
  top: 50%;
  left: 50%;
  width: 400px;
  padding: 40px;
  /* transform: translate(-50%, -50%); */
  background: rgba(0, 0, 0, 0.37);
  box-sizing: border-box;
  /* box-shadow: 0 15px 25px rgba(0,0,0,.6); */
  border-radius: 10px;
  margin-right: auto;
  margin-left: auto;
}

.login-box h2 {
  margin: 0 0 30px;
  padding: 0;
  color: #fff;
  text-align: center;
}

.login-box .user-box {
  position: relative;
}

.login-box .user-box input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  margin-bottom: 30px;
  border: none;
  border-bottom: 1px solid #fff;
  outline: none;
  background: transparent;
}
.login-box .user-box label {
  position: absolute;
  top: 0;
  left: 0;
  padding: 10px 0;
  font-size: 16px;
  color: #fff;
  pointer-events: none;
  transition: 0.5s;
}

.login-box .user-box input:focus ~ label,
.login-box .user-box input:valid ~ label {
  top: -20px;
  left: 0;
  color: #03e9f4;
  font-size: 12px;
}

body {
  margin: 0;
  color: #6a6f8c;
  background: #c8c8c8;
  font: 600 16px/18px "Open Sans", sans-serif;
}
*,
:after,
:before {
  box-sizing: border-box;
}
.clearfix:after,
.clearfix:before {
  content: "";
  display: table;
}
.clearfix:after {
  clear: both;
  display: block;
}
a {
  color: inherit;
  text-decoration: none;
}

.login-wrap {
  width: 100%;
  margin: auto;
  max-width: 525px;
  height: 60vh;
  position: relative;
  background: url(https://raw.githubusercontent.com/khadkamhn/day-01-login-form/master/img/bg.jpg)
    no-repeat center;
  box-shadow: 0 12px 15px 0 rgba(0, 0, 0, 0.24),
    0 17px 50px 0 rgba(0, 0, 0, 0.19);
}
.login-html {
  width: 100%;
  height: 100%;
  position: absolute;
  padding: 20px 70px 50px 70px;
  background: rgba(40, 57, 101, 0.9);
}
.login-html .sign-in-htm,
.login-html .sign-up-htm {
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  position: absolute;
  transform: rotateY(180deg);
  backface-visibility: hidden;
  transition: all 0.4s linear;
}
.login-html .sign-in,
.login-html .sign-up,
.login-form .group .check {
  display: none;
}
.login-html .tab,
.login-form .group .label,
.login-form .group .button {
  text-transform: uppercase;
}
.login-html .tab {
  font-size: 22px;
  margin-right: 15px;
  padding-bottom: 5px;
  margin: 0 15px 10px 0;
  display: inline-block;
  border-bottom: 2px solid transparent;
}
.login-html .sign-in:checked + .tab,
.login-html .sign-up:checked + .tab {
  color: #fff;
  border-color: #1161ee;
}
.button {
  margin-top: 50x;
}
.login-form {
  min-height: 345px;
  position: relative;
  perspective: 1000px;
  transform-style: preserve-3d;
}
.login-form .group {
  margin-bottom: 15px;
}
.login-form .group .label,
.login-form .group .input,
.login-form .group .button {
  width: 100%;
  color: #fff;
  display: block;
}
.login-form .group .input,
.login-form .group .button {
  border: none;
  /* padding:15px 20px; */
  border-radius: 25px;
  background: rgba(255, 255, 255, 0.1);
}
/* .login-form .group input[data-type="password"]{
	text-security:circle;
	-webkit-text-security:circle;
} */
.login-form .group .label {
  color: #aaa;
  font-size: 12px;
}
.login-form .group .button {
  background: #1161ee;
  margin-top: 40px;
}
.login-form .group label .icon {
  width: 15px;
  height: 15px;
  border-radius: 2px;
  position: relative;
  display: inline-block;
  background: rgba(255, 255, 255, 0.1);
}
.login-form .group label .icon:before,
.login-form .group label .icon:after {
  content: "";
  width: 10px;
  height: 2px;
  background: #fff;
  position: absolute;
  transition: all 0.2s ease-in-out 0s;
}
.login-form .group label .icon:before {
  left: 3px;
  width: 5px;
  bottom: 6px;
  transform: scale(0) rotate(0);
}
.login-form .group label .icon:after {
  top: 6px;
  right: 0;
  transform: scale(0) rotate(0);
}
.login-form .group .check:checked + label {
  color: #fff;
}
.login-form .group .check:checked + label .icon {
  background: #1161ee;
}
.login-form .group .check:checked + label .icon:before {
  transform: scale(1) rotate(45deg);
}
.login-form .group .check:checked + label .icon:after {
  transform: scale(1) rotate(-45deg);
}
.login-html
  .sign-in:checked
  + .tab
  + .sign-up
  + .tab
  + .login-form
  .sign-in-htm {
  transform: rotate(0);
}
.login-html .sign-up:checked + .tab + .login-form .sign-up-htm {
  transform: rotate(0);
}

.hr {
  height: 2px;
  margin: 60px 0 50px 0;
  background: rgba(255, 255, 255, 0.2);
}
.foot-lnk {
  text-align: center;
}
</style>
