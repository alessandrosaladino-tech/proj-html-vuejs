<script >
export default {
  data() {
    return {
      menuComponents: ["Home", "Services", "Courses", "About", "FAQ", "Blog", "Contact Us"]
    }
  }
}
</script>

<template>
  <section>
    <header>
      <div class="container">

        <div class="header_top py-2">
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
              <button type="button" class="btn btn-light button_header"><strong>Donate</strong></button>
            </div>
          </div>
        </div>

        <div class="header_bottom py-2">
          <div class="row">
            <div class="col">
              <img src="./assets/img/mt-2236-home-logo.png" alt="">
            </div>
            <div class="col d-flex justify-content-end gap-4">
              <span v-for="component in menuComponents">
                <a href="">{{ component }}</a>
              </span>
            </div>
          </div>
        </div>

      </div>
    </header>

    <div class="jumbotron">
      <div class="container">
        <div class="row">
          <div class="col">

          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  background-image: url(./assets/img/mt-2236-home-bg1.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.header_top span {
  color: white;
  font-size: 14px;
}

.button_header {
  font-size: 14px;
  width: 65%;
}

.header_bottom span {
  font-size: 14px;

  & a {
    text-decoration: none;
    color: white;
  }
}
</style>
