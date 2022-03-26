<template>
  <form @submit.prevent="isCreate ? createService() : updateService(data._id)">
    <ul>
      <li>Tittle</li>
      <li><input v-model="data.title" required type="text" /></li>
      <li>Price</li>
      <li><input v-model="data.price" required type="number" /></li>
      <li>desc</li>
      <li><input v-model="data.desc" required type="text" /></li>
      <li>categories</li>
      <li><input v-model="data.categories" required type="text" /></li>
      <li>img</li>
      <li><input v-model="data.img" required type="text" /></li>
    </ul>

    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">
      Close
    </button>
    <button type="submit" class="btn btn-success">Save changes</button>
  </form>
</template>

<script>
export default {
  name: "Form",
  props: {
    data: {
      type: Object,
      required: true,
    },
    isCreate: {
      type: Boolean,
      required: true,
    },
  },
  methods: {
    createService() {
      if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
      }
      fetch(" https://final-project-backend-2022.herokuapp.com/api/products", {
        method: "POST",
        body: JSON.stringify({
          title: this.data.title,
          categories: this.data.categories,
          desc: this.data.desc,
          img: this.data.img,
          price: this.data.price,
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
          token: `Bearer ${localStorage.getItem("jwt")}`,
        },
      })
        .then((response) => response.json())

        .then((json) => {
          alert("Service added");
          this.$emit("success");
        })
        .catch((err) => {
          console.log(err);
          alert("It failed.Try again please");
          this.loading = false;
        });
    },
    updateService(id) {
      console.log(id);
      if (!localStorage.getItem("jwt")) {
        alert("User not logged in");
      }
      fetch(
        " https://final-project-backend-2022.herokuapp.com/api/products/" + id,
        {
          method: "PUT",
          body: JSON.stringify({
            tittle: this.data.tittle,
            categories: this.data.categories,
            price: this.data.price,
            img: this.data.img,
            desc: this.data.desc,
          }),
          headers: {
            "Content-type": "application/json; charset=UTF-8",
            token: `Bearer ${localStorage.getItem("jwt")}`,
          },
        }
      )
        .then((response) => {
          response.json(), console.log(response.json());
        })
        .then((json) => {
          alert("Service Edited");
          this.$emit("success");
        })
        .catch((err) => {
          alert(err);
        });
    },
  },
};
</script>

<style></style>
