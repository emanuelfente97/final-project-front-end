<template>
  <!-- <section class="header" id="navbar">    -->
  <nav class="navbar navbar-expand-lg fixed-top">
    <img src="../assets/logo5.jpg" class="logo" />
    
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
            <a class="nav-link" href="#about"
              ><i class="fa fa-user"></i> About</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#Skills"
              ><i class="fa fa-bars"></i> Services</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#Timeline"
              ><i class="bi bi-pencil-square"></i>Gallery </a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#cards"
              ><i class="bi bi-file-earmark-code-fill"></i> Team</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#Testimonials"
              ><i class="bi bi-people-fill"></i> Blog</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#Contact"
              ><i class="fa fa-fw fa-envelope"></i>Contacts</a
            >
          </li>
          <div class="but">
            <button type="button" class="btn btn-secondary">Sign in</button>
            &nbsp; &nbsp;
            <button type="button" class="btn btn-secondary">Sign up</button>
          </div>
        </ul>
      </div>
    
  </nav>
  <!-- </section> -->
</template>

<script>
export default {};
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
  background-color: transparent;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  /* height:20px !important; */
  z-index: 9999999999999999;
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
.but {position: relative; left:10%}
  
}
</style>
