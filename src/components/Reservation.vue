<template>
  <div id="hide">
    <section id="reservation">
      <div
        class="container mt-5"
        style="justify-content: center; position: fixed"
      >
        <div class="row">
          <div class="col-md-6 offset-md-3 border p-4 shadow bg-light">
            <div class="col-12">
              <h3 class="fw-normal text-secondary fs-4 text-uppercase mb-4">
                Reservation Form
              </h3>
            </div>
            <form @submit.prevent="handleSubmit">
              <div class="row g-3">
                <div class="col-md-6">
                  <input
                    type="text"
                    required
                    class="form-control"
                    v-model="name"
                    placeholder="Name"
                  />
                </div>

                <div class="col-md-6">
                  <input
                    type="email"
                    v-model="email"
                    required
                    class="form-control"
                    placeholder="Enter Email"
                  />
                </div>
                <div class="col-md-6">
                  <input
                    type="date"
                    v-model="date"
                    required
                    class="form-control"
                    placeholder="Enter Date"
                  />
                </div>
                <div class="col-md-6">
                  <input
                    type="time"
                    v-model="time"
                    required
                    class="form-control"
                    placeholder="Enter Email"
                  />
                </div>
                <div class="col-12">
                  <select class="form-select">
                    <option selected="">Purpose Of Appointment</option>
                    <option value="1">Hair Cut</option>
                    <option value="2">Special Treat</option>
                    <option value="3">Other Services</option>
                  </select>
                </div>
                <div class="col-12">
                  <textarea
                    class="form-control"
                    placeholder="Message"
                  ></textarea>
                </div>
                <div class="col-12 mt-5">
                  <button type="submit" class="btn btn-primary float-end">
                    Submit
                  </button>
                  <a
                    class="btn btn-outline-secondary float-end me-2"
                    style="background-color: #b23cfd; color: #fff"
                    href="/"
                    >cancel</a
                  >
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      surname: "",
      date: "",
      time: "",
      message: "",
      form: false,
    };
  },
  mounted() {
    if (!localStorage.getItem("jwt")) {
      alert("User not logged in");
      return location.reload();
    }
  },
  methods: {
    showForm() {
      this.form = !this.form;
    },

    handleSubmit() {
      (this.name, this.surname, this.email, this.date, this.message, this.time),
        fetch("https://final-project-backend-2022.herokuapp.com/api/contacts", {
          method: "POST",
          headers: { "Content-type": "application/json; charset=UTF-8" },
          body: JSON.stringify({
            name: this.name,
            surname: this.surname,
            email: this.email,
            time: this.time,
            message: this.message,
          }),
        })
          .then((response) => response.json())
          .then((json) => console.log(json.msg))
          .catch((err) => console.log(err.msg));
    },
  },
};
</script>

<style scoped>
.bg-light {
  background-color: rgba(40, 57, 101, 0.9) !important;
}
</style>
