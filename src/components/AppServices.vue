<script>
import AppButton from './AppButton.vue';
export default {
    name: "AppServices",
    components: {
        AppButton,
    },

    data() {
        return {
            listItems: ["Build self-regulation and motivation", "Help with concentration issues", "Learn to plan, organize and prioritize", "Regulate emotions", "Learn to pay attention to detail"],
            chessImg: "../src/assets/img/mt-2236-home-icon-bullet.png",

            servicesItem: [
                {
                    img: "../src/assets/img/mt-2236-home-icon1.png",
                    title: "Various Age Groups",
                    bio: "We provide chess classes to both children from 5 years old and adults.",
                },
                {
                    img: "../src/assets/img/mt-2236-home-icon2.png",
                    title: "Top Chess Variants",
                    bio: "We don't only teach classical chess but also other top variants of this game.",
                },
                {
                    img: "../src/assets/img/mt-2236-home-icon3.png",
                    title: "Best Chess Players",
                    bio: "Our alumni have won many prestigious chess tournaments in the contry.",
                },
                {
                    img: "../src/assets/img/mt-2236-home-icon4.png",
                    title: "Best Chess Openings",
                    bio: "Our students know all the best chess openings and how tu use them.",
                },


            ]
        }
    }
}
</script>

<template>
    <div class="container services">
        <div class="div text-center pb-4">
            <h1 class="fw-bold ">OUR SERVICES</h1>
            <p class="bg_secondary text">We make your child happy day after day</p>
        </div>
        <div class="row">
            <div class="col-4">
                <h4 class="fw-semibold">Chess Education</h4>
                <h5 class="">Popular education for your child and you</h5>
                <p class="bg_secondary">Teacher and parents around the world know that chess is not a simple game, it is a
                    great learning tool
                    that will help build your child's executive function skills.</p>
                <ul class="p-0 px-3">
                    <li v-for="item in listItems" class="">
                        <img :src="chessImg" alt="">
                        <span class="ps-3">{{ item }}</span>
                    </li>
                </ul>
                <AppButton class="bg_primary mt-3">Learn More</AppButton>
            </div>
            <div class="col-8 d-flex flex-wrap justify-content-around">
                <div class="container_cards d-flex flex-column flex-wrap" v-for="item in servicesItem">
                    <img :src="item.img" alt="">
                    <h6 class="fw-semibold">{{ item.title }}</h6>
                    <p class="bg_secondary">{{ item.bio }}</p>
                </div>
            </div>

        </div>

    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.services {
    padding-top: 7rem;
    padding-bottom: 7rem;
}

p {
    color: $chess_text;
}

li {
    list-style-type: none;

    & span {
        color: $chess_text;
    }
}

.btn_learn {
    width: 53%
}

.container_cards {
    width: 43%;
    padding-left: 3rem;

    & img {
        width: 15%;
    }

    & h6 {
        padding-top: 10px;
    }

    & p {
        padding-top: 1px;
    }
}

.text {
    font-size: 23px;
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