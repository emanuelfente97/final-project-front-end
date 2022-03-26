<template>
  <section id="services">
    <div class="container">
      <h1 id="title" style="font-size: 45px"><strong>Services</strong></h1>
      <div class="details">
        <p class="cheat">We Offer the following services</p>
        <!-- Button trigger modal -->
        <button
          v-if="isAdmin"
          type="button"
          class="btn btn-none"
          data-bs-toggle="modal"
          data-bs-target="#exampleModal2"
        >
          Add Services</button
        >&nbsp;&nbsp;
        <label
          >Sort Price:
          <select
            style="height: 30px"
            v-model="price"
            @change="sortPrice(price)"
          >
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
          </select>
        </label>
        &nbsp;&nbsp;
        <label>
          Sort Name:
          <select
            style="height: 30px"
            v-model="title"
            @change="sortTitle(title)"
          >
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
          </select>
        </label>

        <!-- Create Modal -->
        <div
          class="modal fade"
          ref="updateModal"
          id="exampleModal2"
          tabindex="-1"
          aria-labelledby="exampleModalLabel2"
          aria-hidden="true"
        >
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel2">Modal title</h5>
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div class="modal-body">
                <FormComponent
                  :data="{}"
                  :isCreate="true"
                  @success="getServices()"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="main-box">
        <div
          class="box box-red mx-auto"
          v-for="product in products"
          :key="product._id"
        >
          <div class="icon">
            <img
              :src="product.img"
              alt="pik"
              style="width: 100px; height: 100px; border-radius: 50%"
            />
          </div>
          <h3>{{ product.title }}</h3>
          <hr />

          <p>
            {{ product.desc }}
          </p>
          <button
            type="button"
            class="btn"
            style="border-color: #0db8de;
    color: #0db8de;
    border-radius: 0px;
    font-weight: bold;
    letter-spacing: 1px;
    box-shadow: 0 1px 3px rgb(0 0 0 / 12%), 0 1px 2px rgb(0 0 0 / 24%);
}"
          >
            R {{ product.price }}</button
          >&nbsp;
          <button
            v-if="isAdmin"
            type="button"
            class="btn"
            style="border-color: #0db8de;
    color: #0db8de;
    border-radius: 0px;
    font-weight: bold;
    letter-spacing: 1px;
    box-shadow: 0 1px 3px rgb(0 0 0 / 12%), 0 1px 2px rgb(0 0 0 / 24%);
}"
            v-on:click="removeService(product._id)"
          >
            Delete</button
          >&nbsp;
          <button
            v-if="isAdmin"
            @click="update(product)"
            type="button"
            style="border-color: #0db8de;
    color: #0db8de;
    border-radius: 0px;
    font-weight: bold;
    letter-spacing: 1px;
    box-shadow: 0 1px 3px rgb(0 0 0 / 12%), 0 1px 2px rgb(0 0 0 / 24%);
}"
            class="btn"
            data-bs-toggle="modal"
            data-bs-target="#exampleModal4"
          >
            Update
          </button>
        </div>

        <!-- MOdal For Update -->
        <div
          class="modal fade"
          id="exampleModal4"
          tabindex="-1"
          aria-labelledby="exampleModalLabel4"
          aria-hidden="true"
        >
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel4">Edit Note</h5>

                <button
                  type="button"
                  class="btn-close btn-danger"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>

              <div class="modal-body">
                <FormComponent :data="form" :isCreate="false" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import FormComponent from "./servicesComponents/formComponent.vue";
export default {
  components: {
    FormComponent,
  },
  data() {
    return {
      form: {},
      products: null,
      userLoggedIn: false,
      isAdmin: false,
    };
  },
  mounted() {
    if (localStorage.getItem("jwt")) {
      this.userLoggedIn = true;
    }

    console.log(localStorage.getItem("isAdmin"));
    if (localStorage.getItem("isAdmin") === "true") {
      this.isAdmin = true;
    }

    this.getServices();
  },

  computed: {
    filterProducts: function () {
      return this.products.filter((product) => {
        return product.category.toLowerCase().match(this.search.toLowerCase());
      });
    },
  },
  methods: {
    getServices() {
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

    removeService(id) {
      if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
      }
      console.log(id);
      fetch(
        "https://final-project-backend-2022.herokuapp.com/api/products/" + id,
        {
          method: "DELETE",
          headers: {
            "Content-type": "application/json; charset=UTF-8",
            token: `Bearer ${localStorage.getItem("jwt")}`,
          },
        }
      )
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
          this.getServices();
          alert("Service removed successfully");
        })
        .catch((error) => {
          console.error("Error:", error);
        });
    },
    update(product) {
      this.form = product;
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
#services {
  padding-top: 65px;
}
button {
  margin-top: 10px;
}
.container {
  width: 80%;
  margin: 0 auto;
}
.details {
  text-align: center;
}
.cheat {
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
  color: #2c3e50;
  text-align: center;
  font-size: 30px;
  max-width: 420px;
  position: relative;
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
  /* z-index: 10000; */
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
.modal-backdrop {
  z-index: 10000;
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
  background-color: #9b9be2;
}
.box-red {
  background-color: rgb(128, 128, 128);
}
.container {
  width: 80%;
}
</style>
