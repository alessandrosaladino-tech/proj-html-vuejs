<script>
import AppButton from './AppButton.vue';
export default {
    name: "AppJumbotron",
    components:{
      AppButton,
    }
}
</script>

<template>

 <div class="jumbotron p-5">
      <div class="container py_">
        <div class="row">
          <div class="col-6">
            <span class="badge rounded-pill text-bg-warning">WELCOME</span>
            <h1 class="">ACADEMIC CHESS FOR <i>EVERYONE</i> </h1>
            <span>We are dedicated to broadening and developing chess as art, recreation, and as a significant element of
              culture in Northern California.</span>
            <div class="d-flex py-4 gap-3">
              <AppButton class="bg_primary">Enroll Now</AppButton>
              <AppButton class="bg_transparent">Learn More</AppButton>
            </div>
          </div>
        </div>
      </div>
    </div>

</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

jumbotron h1,span {
  color: $chess_accent;
  font-size: 20px;
}

jumbotron .col-6, h1 {
  color: $chess_white;
  font-size: 60px;
  font-weight: 600;
  padding-top: 13px;

  & h1, i {
    color: $chess_primary;

  }
}

.py_ {
  padding-top: 10rem;
  padding-bottom: 10rem;
}

/* Buttons */
.bg_primary {
  background-color: $chess_primary;
  border: none;
}
.bg_primary:hover {
 background-color: $chess_secondary;
 color: $chess_primary;
}
.bg_transparent {
  background-color: transparent;
  border: 1px solid $chess_white;
  color: white;
}

.bg_transparent:hover {
  background-color: $chess_white;
  color: black;
}

</style>