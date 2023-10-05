<script>
import AppButton from './AppButton.vue';
export default {
    components: {
        AppButton,
    },
    data() {
        return {
            events: [
                {
                    img: "../src/assets/img/mt-2236-home-img4.jpg",
                    title: "Grand Summer Tournament of 2021",
                    bio: "Join us for the Grand Summer Tournament 2021. Held every year on the first Sunday of summer, our grand Summer Tournament chess masters and beginners from North California. We have competition for different levels of chess mastery with amazing prizes awarded at each level.",
                },
                {
                    img: "../src/assets/img/mt-2236-home-img5.jpg",
                    title: "World Chess Day",
                    bio: "Celebrated on July 20 every year, World Chess Day is one of the biggest events at out school. Be ready for fun tournaments and big prizes. Registration is obligatory!",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container text-center p_top">
        <h1 class="fw-bold">Our Events</h1>
        <p class="pb-5 text_color">Chess is fun and we are happy to prove it at our events!</p>

        <div class="row g-0 align-items-center pb-5" v-for="event in events">
            <div class="col">
                <img :src="event.img" alt="">
            </div>
            <div class="col text-start">
                <h4 class="fw-bold">{{ event.title }}</h4>
                <p>{{ event.bio }}</p>
            </div>
            <div class="col">
                <AppButton class="bg_primary">Register</AppButton>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.row p {
    font-size: 13.5px;
    color: $chess_text;

}

.p_top {
    padding-top: 5rem;
    padding-bottom: 3rem;
}

.text_color {
    color: $chess_text;
    font-size: 23px;
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
</style>