        
<script>
import AppButton from './AppButton.vue';
export default {
    components: {
        AppButton
    },
    data() {
        return {
            imgBanner: ["../src/assets/img/mt-2236-home-gallery1.jpg", "../src/assets/img/mt-2236-home-gallery2.jpg", "../src/assets/img/mt-2236-home-gallery3.jpg", "../src/assets/img/mt-2236-home-gallery4.jpg"]
        }
    }
}
</script>


<template>

    <!--4 img banner start-->
    <div class="container_banner">
        <div class="row gx-0">
            <div class="col " v-for="img in imgBanner">
                <img :src="img" alt="">
            </div>
        </div>
    </div>
    <!--4 img banner end-->

    <!--Play and learn-->
    <div class="container_play_learn">
        <div class="container pt-5 pb-5">
            <div class="row align-items-center">
                <div class="col-2 d-flex justify-content-center">
                    <img src="../assets/img/mt-2236-home-icon5.png" alt="">
                </div>
                <div class="col-7 pt-3">
                    <h1 class="fw-bold">PLAY & LEARN</h1>
                    <p class="fw-light">Take a look into our day to day life here at Chess School</p>
                </div>
                <div class="col-3">
                    <AppButton class="bg_primary">Lean More</AppButton>
                </div>
            </div>
        </div>
    </div>
    <!--Play and learn end-->


</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.col, img {
    width: 100%;
}

.container_play_learn {
    background-color: $chess_primary;
    display: flex;
    align-items: center;

    & img {
        width: 45%;
    }

    & p {
        font-size: 25px;
    }
}

/* Button */
.bg_primary {
  background-color: $chess_primary;
}
.bg_primary:hover {
 background-color: $chess_secondary;
 color: $chess_primary;
}
</style>