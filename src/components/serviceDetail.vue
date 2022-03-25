<template>
  <section id="services">
  

<!-- add -->


      
 <!-- get -->




  <div class="container">
      <h1>Services</h1>
    <div class="details">
    
      <p class="cheat">We Offer the following services</p>
      <!-- Button trigger modal -->
<button type="button" class="btn btn-none" data-bs-toggle="modal" data-bs-target="#exampleModal2"> Update
</button>&nbsp;&nbsp; <label>Sort Price:
          <select style="height:30px" v-model="price" @change="sortPrice(price)">
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
          </select>
        </label>
        &nbsp;&nbsp;
        <label>
          Sort Name:
          <select style="height:30px" v-model="title" @change="sortTitle(title)">
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
          </select>
        </label>


<!-- Modal -->
<div class="modal fade" id="exampleModal2" tabindex="-1" aria-labelledby="exampleModalLabel2" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel2">Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
         <form @submit.prevent="createService">
        <ul>
         <li>Tittle </li>
          <li> <input v-model="title" required type="text"></li>
          <li>Price</li>
          <li> <input v-model="price" required type="number"></li>
        <li>desc</li>
        <li> <input v-model="desc" required type="text"></li>
        <li>categories</li>
        <li> <input v-model="categories" required type="text"></li>
        <li>img</li>
        <li> <input v-model="img" required type="text"></li>
       </ul>
       <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="submit" class="btn btn-success">Add Service</button>
        
       </form>
      </div>
      
    </div>
  </div>
</div>
    </div>
    <div class="main-box" >
      <div class="box box-red mx-auto" v-for="product in products" :key="product._id" >
        <div class="icon">
          <img :src="product.img" alt="pik" 
            
            style="width: 100px; height: 100px; border-radius: 50%">
          <!-- <img
            class="img"
            src="https://i.postimg.cc/MKft6bpP/facials.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          /> -->
        </div>
           <h3> {{product.title}} </h3>
        <hr />
        <p>
          {{product.desc}}
         <!-- A realxing treatment that cleanses, revujenates and moisturises the skin to reveal the inner glow.
         Your face will thank you. -->
        </p>
        <button type="button" class="btn btn-secondary" data-bs-toggle="modal" data-bs-target="#exampleModal4">Update</button>&nbsp;
        <button type="button" class="btn btn-secondary">R{{product.price}}</button>
                <!-- <button type="button" class="btn btn-secondary" v-on:click="removeService(product._id)">Delete</button> -->
      </div>
</template>

<script>
export default {
    
     mounted() {
    fetch("https://capstone-bkend.herokuapp.com/products/" + this.id, {
      method: "GET",
      headers: {
        "Content-type": "application/json; charset=UTF-8",
      },
    })
      .then((response) => response.json())
      .then((json) => {
        this.product = json;
      })
      .catch((err) => {
        alert(console.log(err));
      });
  },
};


</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
#services{
  padding-top:65px
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
  width: 100%;
  justify-content: center;
  flex-wrap: wrap;
}
.box {
  width: 32%;
  margin: 60px;
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