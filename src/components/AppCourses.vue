<script>
import AppButton from './AppButton.vue';
export default {
    components: {
        AppButton,
    },
    data() {
        return {
            courses: [
                {
                    img: "../src/assets/img/mt-2236-home-img1.jpg",
                    title: "Garry Kasparov's Masterclass",
                    bio: "Learn the tips,tricks, and strategies from one of the best masters",
                    price: "$456",
                },
                {
                    img: "../src/assets/img/mt-2236-home-img2.jpg",
                    title: "Online Chess Lessons for Beginners",
                    bio: "Catered to adult beginners who have a few hours a week to practice",
                    price: "$205",
                },
                {
                    img: "../src/assets/img/mt-2236-home-img3.jpg",
                    title: "International Chess School Online",
                    bio: "Chess lessons for childern and adults held completely online",
                    price: "$356",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container text-center courses">
        <div class="container text-center pb-3">
            <h1 class="fw-bold">Courses</h1>
            <p class="text">To keep up with the constantly rising standards of play</p>
        </div>
        <div class="container d-flex gap-4">
            <div class="card  courses_card" v-for="course in courses">
                <div class="card-img">
                    <img :src="course.img" alt="">
                </div>
                <div class="card-body  text-center">
                    <h3 class="fw-bold">{{ course.title }}</h3>
                    <p>{{ course.bio }}</p>
                    <p class="price">{{ course.price }}</p>
                    <AppButton class="bg_primary">View More</AppButton>
                </div>
            </div>
        </div>

        <button type="button" class="button_courses">View Other Courses</button>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.card,
img {
    width: 100%;

}

.courses {
    margin-top: 5rem;
    margin-bottom: 1rem;
}

p {
    color: $chess_text;
}

.price {
    font-weight: bolder;
    color: black;
    font-size: 20px;
}

.courses_card {
    box-shadow: 0px 2px 9px $chess_secondary;
    border-radius: 3px;
}

.courses_card:hover {
    transform: scale(1.1);
    transition: 1s;
}

.text {
    font-size: 23px;
}

/* Buttons */
.bg_primary {
  background-color: $chess_primary;
  border: none;
  margin-bottom: 15px;
}
.bg_primary:hover {
 background-color: $chess_secondary;
 color: $chess_primary;
}

.button_courses {
    width: 250px;
    height: 50px;
    margin-top: 50px;
    margin-bottom: 50px;
    font-weight: bold;
    background-color: $chess_white;
    border-radius: 8px;
}

.button_courses:hover {
    background-color: $chess_primary;
    color: $chess_white;
    border: none
}

</style>