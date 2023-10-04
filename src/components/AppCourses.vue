<script>
export default {
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
            <p>To keep up with the constantly rising standards of play</p>
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
                    <button type="button" class="btn btn-warning fw-bold">View More</button>
                </div>
            </div>
        </div>

        <button type="button" class="btn btn-outline-dark m-5">View Other Courses</button>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.card, img {
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
    font-weight: bold;
    color: black;
}

.courses_card {
    border-bottom: 2px solid #9a9595ae;
    border-radius: 3px;
}

</style>