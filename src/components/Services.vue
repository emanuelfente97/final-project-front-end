<template>
<section id="services">
  

<!-- add -->


      
 <!-- get -->




  <div class="container">
      <h1>Services</h1>
    <div class="details">
    
      <p class="cheat">We Offer the following services</p>
      <!-- Button trigger modal -->
<button type="button" class="btn btn-none" data-bs-toggle="modal" data-bs-target="#exampleModal2"> Add Services
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
        <button type="button" class="btn btn-secondary" data-bs-toggle="modal" data-bs-target="#exampleModal4">View Service</button>&nbsp;
        <!-- <button type="button" class="btn btn-secondary">R{{product.price}}</button> -->
                <button type="button" class="btn btn-secondary" v-on:click="removeService(product._id)">Delete</button>
      </div>

    <!-- MOdal For Update -->
<div class="modal fade" id="exampleModal4" tabindex="-1" aria-labelledby="exampleModalLabel4" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel4">Edit Note</h5>
        
        <button type="button" class="btn-close btn-danger" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>

      <div class="modal-body">
       <form @submit.prevent="updateService(+ id)">
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
          <button type="submit"  class="btn btn-success">Save changes</button>
        
       </form>
      </div>
     
    </div>
  </div>
</div>
      <!-- <div class="box box-grey mx-auto">
        <img
          class="img"
          src="https://i.postimg.cc/rmqPvz69/beard-trim.jpg"
          style="width: 100px; height: 100px; border-radius: 50%"
        />

        <h2>Beard Trim</h2>
        <hr />
        <p>
         Let your Tame face manee to your liking and give you the jaw line you were destined to have. 
        </p>
        <button type="button" class="btn btn-secondary">Book</button>&nbsp;
        <button type="button" class="btn btn-secondary">R25</button>
      </div>

      <div class="box box-red mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/hPFc5by8/hair-cut.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Hair Cut</h2>
        <hr />
        <p>
   Our Hair cut comes with a shampoo and conditioning tretment, neck shave and very comfortable couches.
        </p>
        <button type="button" class="btn btn-secondary">Book</button>&nbsp;
        <button type="button" class="btn btn-secondary">R25</button>

      </div>

      <div class="box box-grey mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/7Yv5hn78/waxing.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Coloring</h2>
        <hr />
        <p>
        We will blend away your gray hairs to create a younger natural-looking you. Who can't turn back time?

        </p>
        <button type="button" class="btn btn-secondary">Book</button>&nbsp;
        <button type="button" class="btn btn-secondary">R25</button>
      </div>
      <div class="box box-red mx-auto">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/XvQszCFc/hair-cut-and-trim.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Hair Cut and Trim </h2>
        <hr />
        <p>
         No bad hair days here. Everything you need to stay fresh and so clean. Take it up a notch with a premium, nourishing hair treatment add-on.
        </p>;
        <button type="button" class="btn btn-secondary">Book</button>&nbsp;
        <button type="button" class="btn btn-secondary">R25</button>
      </div>

      <div class="box box-grey mx-auto" style="background-image: url(https://i.postimg.cc/C14nNGqS/backgraound.jpg);">
        <div class="icon">
          <img
            class="img"
            src="https://i.postimg.cc/QMzvw1fS/services1.jpg"
            style="width: 100px; height: 100px; border-radius: 50%"
          />
        </div>
        <h2>Wash</h2>
        <hr />
        <p>
          Struggling to wash your hair? Legends barber shop provide the best service that comes with shampoo, hair conditioning and comfortable seats. 
        </p>
        <button type="button" class="btn btn-secondary">Book</button>&nbsp;
        <button type="button" class="btn btn-secondary">R25</button>

      </div>
    </div> -->
    </div>
  </div>
</section>
</template>

<script>
export default {
data() {
    return {
       title: "",
    desc: "",
    img: "",
    categories: "",
    price: "",
    products:null
    };
  },
  mounted() {
    fetch(" https://final-project-backend-2022.herokuapp.com/api/products", {
      method: "GET",
      headers: {
        "Content-type": "application/json; charset=UTF-8",
      },
    })
      .then((response) => response.json())
      .then((json) => {
        this.products = json;
      });
  },
 
  computed: {
    filterProducts: function () {
      return this.products.filter((product) => {
        return product.category.toLowerCase().match(this.search.toLowerCase());
      });
    },
  },
  methods: {
    sortPrice(price) {
      this.filterProducts = this.filterProducts.sort(
        (a, b) => a.price - b.price
      );
      if (price == "desc") this.filterProducts.reverse();
    },
    sortTitle(title) {
      this.filterProducts = this.filterProducts.sort((a, b) => {
        if (a.title.toLowerCase() < b.title.toLowerCase()) {
          return -1;
        }
        if (a.title.toLowerCase() > b.title.toLowerCase()) {
          return 1;
        }
        return 0;
      });
      if (title == "desc") this.filterProducts.reverse();
    },
    filterCategory(category) {
      if (category) {
        this.filterProducts = this.products.filter(
          (product) => product.category == category
        );
      } else {
        this.filterProducts = this.products;
      }
    },
  //  add
     createService() {
        
      if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
       
      }
    fetch(" https://final-project-backend-2022.herokuapp.com/api/products", {
        method: "POST",
        body: JSON.stringify({
          title: this.title,
          categories: this.categories,
          desc: this.desc,
          img:this.img,
          price: this.price,

    
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
          token: `Bearer ${localStorage.getItem("jwt")}`,
        },
      })
        .then((response) => response.json())
    
        .then((json) => {
         
          alert("Service added");
         
        })
        .catch((err) => {
          console.log(err)
          alert("It failed.Try again please");
          this.loading = false;
        });
    },

    //Update
     updateService() {
      if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
      }
      fetch(" https://final-project-backend-2022.herokuapp.com/api/products" + id, {
        method: "PUT",
        body: JSON.stringify({
          tittle: this.tittle,
          categories: this.categories,
          price: this.price,
          img: this.img,
          desc: this.desc
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
          token: `Bearer ${localStorage.getItem("jwt")}`,
        },
      })
        .then((response) => response.json())
        .then((json) => {
          alert("Service Edited");
        })
        .catch((err) => {
          alert(err);
        });
    },

    //Delete

 removeService(id) {
    if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
      }
      console.log(id);
      fetch("https://final-project-backend-2022.herokuapp.com/api/products/" + id, {
        method: "DELETE",
          headers: {
          "Content-type": "application/json; charset=UTF-8",
          token: `Bearer ${localStorage.getItem("jwt")}`,
        },
      })
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
          alert("Service removed successfully");
        })
        .catch((error) => {
          console.error("Error:", error);
        });
    },
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
