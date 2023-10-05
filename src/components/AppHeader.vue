<script>
import AppPhone from './AppPhone.vue';
import AppButton from './AppButton.vue'
export default {
  name: "AppHeader",
  data() {
    return {
      menuComponents: ["Home", "Services", "Courses", "About", "FAQ", "Blog", "Contact Us"]
    }
  },

  components: {
    AppPhone,
    AppButton,
  }
}
</script>

<template>
  <header>
    <div class="container">

      <div class="header_top py-2">
        <!--Prima Row-->
        <div class="row align-items-center ">

          <div class="col-6 d-flex gap-2 r align-items-center ">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="yellow" class="bi bi-geo-alt-fill"
              viewBox="0 0 16 16">
              <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10zm0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6z" />
            </svg>
            <span>6767 Santa Monica Blvd, Los Angeles, CA 90038</span>
          </div>

          <div class="col d-flex justify-content-end align-items-center gap-2 me-5">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="yellow" class="bi bi-telephone-fill"
              viewBox="0 0 16 16">
              <path fill-rule="evenodd"
                d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z" />
            </svg>
            <span>Call Now 123-456-7890</span>
          </div>

          <div class="col d-flex justify-content-end align-items-center ">
            <AppButton class="btn_header">Donate</AppButton>
          </div>
        </div>
      </div>



      <div class="header_bottom pb-3 pt-1">
        <!--Seconda row-->
        <div class="row">
          <div class="col">
            <img src="../assets/img/mt-2236-home-logo.png" alt="">
          </div>
          <div class="col d-flex justify-content-end gap-3">
            <span v-for="component in menuComponents">
              <a href="#" class="active">{{ component }}</a>
            </span>
          </div>
        </div>
      </div>

    </div>
    
    <AppPhone></AppPhone>
  </header>

</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

header {
  background-color: #0506205b;
}

.header_top span {
  color: $chess_accent;
  font-size: 14px;
}

.header_bottom span {
  font-size: 14px;

  & a {
    text-decoration: none;
    color: $chess_accent;
  }

  .active:hover {
    color: $chess_primary;
    border-bottom: 1px solid $chess_primary;
  }

}

header {
  position: fixed;
  width: 100%;
  margin-bottom: 2rem;
}

/* Button */
.btn_header {
  width: 150px;
  height: 40px;
  border-radius: 11px;
  border: none
}

.btn_header:hover {
  background-color: $chess_secondary;
  color: $chess_primary;
}
</style>
