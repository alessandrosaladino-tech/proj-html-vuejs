<script>
export default {
    name: "AppJumbotron",
}
</script>

<template>

 <div class="jumbotron p-5">
      <div class="container py-5">
        <div class="row">
          <div class="col-6">
            <span class="badge rounded-pill text-bg-warning">WELCOME</span>
            <h1 class="">ACADEMIC CHESS FOR <i>EVERYONE</i> </h1>
            <span>We are dedicated to broadening and developing chess as art, recreation, and as a significant element of
              culture in Northern California.</span>
            <div class="d-flex py-4 gap-3">
              <button type="button" class="btn btn-warning"><strong>Enroll Now</strong></button>
              <button type="button" class="btn btn-outline-light"><strong>Learn More</strong></button>
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


</style>