<script>
export default {
    name: "AppNews",
    data() {
        return {
            news: [
                {
                    img: "../src/assets/img/mt-2236-blog-img1.jpg",
                    bio: "The most common mistakes when managing personal finances",
                },
                {
                    img: "../src/assets/img/mt-2236-blog-img2.jpg",
                    bio: "Methods of the recruitment",
                },
            ]
        }
    }
}
</script>

<template>
    <section class="news">
        <div class="container d-flex news_container">
            <div class=" d-flex gap-4">
                <div class="col-4">
                    <div class="box">
                        <h1 class="fw-bold ">Latest News</h1>
                        <div class="border_news"></div>
                    </div>

                    <button type="button" class="btn btn-outline-dark fw-bold">View Other Posts</button>
                </div>
                <div class="col " v-for="item in news">
                    <img :src="item.img" alt="">
                    <p class="pt-3">{{ item.bio }}</p>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;

.news {
    background-color: #f8f7f7;

    & .news_container {
        padding-top: 7rem;
        padding-bottom: 5rem;
    }

    & .border_news {
        border-bottom: 2px solid $chess_primary;
        width: 20%;
        padding-top: 2rem;
        margin-bottom: 2.8rem;
    }
}


.col4,
img {
    width: 100%;
}
</style>