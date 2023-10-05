<script>
import AppButton from './AppButton.vue';
export default {
components: {
    AppButton,
}
}
</script>

<template>
    <div class="container_firststep">
        <div class="container d-flex firststep_padding ">
            <div class="container">
                <h1 class="fw-bold">TAKE THE <span>FIRST STEP</span></h1>
                <p>The fascinating world of chess has its doors open for anyone</p>
            </div>
            <div class="container_button">
                <AppButton class="bg_primary">View More</AppButton>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.container_firststep {
    background-image: url("../src/assets/img/mt-2236-home-bg2.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    & h1 {
        color: $chess_white;
    }

    & span {
        color: $chess_primary;
    }

    & p {
        color: $chess_text;
    }
}

.firststep_padding {
    padding-top: 4rem;
    padding-bottom: 4rem;
    align-items: center;
}

.button_width {
     width: 35%;
}

.container_button {
    width: 50%;
    display: flex;
    justify-content: center;
}

/* Button */
.bg_primary {
  background-color: $chess_primary;
  border: none;
}
.bg_primary:hover {
 background-color: $chess_secondary;
 color: $chess_primary;
}
</style>