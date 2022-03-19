<template>
  <div class="container mt-5" style="justify-content: center; position: fixed">
    <div class="row">
      <div class="col-md-6 offset-md-3 border p-4 shadow bg-light">
        <div class="col-12">
          <h3 class="fw-normal text-secondary fs-4 text-uppercase mb-4">
            Reservation Form
          </h3>
        </div>
        <form action="">
          <div class="row g-3">
            <div class="col-md-6">
              <input
                type="text"
                class="form-control"
                placeholder="First Name"
              />
            </div>
            <div class="col-md-6">
              <input type="text" class="form-control" placeholder="Last Name" />
            </div>
            <div class="col-md-6">
              <input
                type="tel"
                class="form-control"
                placeholder="Phone Number"
              />
            </div>
            <div class="col-md-6">
              <input
                type="email"
                class="form-control"
                placeholder="Enter Email"
              />
            </div>
            <div class="col-md-6">
              <input
                type="date"
                class="form-control"
                placeholder="Enter Date"
              />
            </div>
            <div class="col-md-6">
              <input
                type="time"
                class="form-control"
                placeholder="Enter Email"
              />
            </div>
            <div class="col-12">
              <select class="form-select">
                <option selected="">Purpose Of Appointment</option>
                <option value="1">Web Design</option>
                <option value="2">Web Development</option>
                <option value="3">IOS Developemt</option>
              </select>
            </div>
            <div class="col-12">
              <textarea class="form-control" placeholder="Message"></textarea>
            </div>
            <div class="col-12 mt-5">
              <button type="submit" class="btn btn-primary float-end">
                Book Appointment
              </button>
              <a class="btn btn-outline-secondary float-end me-2" style="background-color: #b23cfd; color:#fff" href="/"
                >cancel</a
              >
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: false,
    };
  },

  methods: {
    methods: {
      showForm() {
        this.form = !this.form;
      },
    },
  },
};
</script>

<style scoped>
.bg-light {
  background-color: rgba(40, 57, 101, 0.9) !important;
}
</style>
