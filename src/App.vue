<script >
import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  data() {
    return {
    }
  },

  components: {
    AppHeader,
    AppJumbotron,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
  <section class="header_section">
    <AppHeader></AppHeader>
    <AppJumbotron></AppJumbotron>
  </section>

  <AppMain></AppMain>

  <section id="footer_section">
    <AppFooter></AppFooter>
  </section>

</template>

<style lang="scss" scoped>
@use "./assets/scss/partials/variables" as *;

.header_section {
  background-image: url(./assets/img/mt-2236-home-bg1.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: bottom;
}

#footer_section{
  background-color: $chess_secondary;
  color: $chess_white;
}
</style>
