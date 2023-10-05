<script>
import AppButton from './AppButton.vue';
export default {
    components: {
    AppButton,
    },
    data() {
        return {

            icons: ["../src/assets/img/facebook-f.svg", "../src/assets/img/telegram.svg", "../src/assets/img/instagram.svg"],
            siteLogo: "../src/assets/img/mt-2236-home-logo.png",
            copyright: `Copyright &copy; 2021.All Rights Reserved.`,
            subscribedEmail: "",
            emailList: [],
        }

    },

    methods: {
        addEmail() {
            
            this.emailList.push(this.subscribedEmail);
            console.log(this.subscribedEmail);
            console.log(this.emailList);
            this.subscribedEmail = "";
        }
    }
}
</script>

<template>
    <div class="container d-flex pt-5 pb-4">
        <div class="col">
            <img :src="siteLogo" alt="" class="site_img">
            <p>{{ copyright }}</p>
        </div>
        <div class="col">
            <h4 class="fw-bold pb-4">Follow Us</h4>
            <div class="container_icon">
                <div class="chess-icon d-flex" v-for="icon in icons">
                    <img :src="icon" alt="" class="filter_icon">
                </div>
            </div>
        </div>
        <div class="col d-flex flex-column gap-3">
            <h4 class="m-0 fw-bold">Subscribe to get the latest news, course updates, discounts,events</h4>
            <input type="text" placeholder="Enter your e-mail here*" v-model="subscribedEmail" @keyup.enter="addEmail">
            <AppButton class="bg_primary" @click="addEmail">Subscribe</AppButton>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../assets/scss/partials/variables" as *;


.chess-icon {
    width: 35px;
    height: 35px;
    border: 1px solid $chess_white;
    padding: 7px;
    border-radius: 3px;
    display: flex;
    justify-content: center;
    background-color: transparent;

}

.chess-icon:hover {
    background-color: $chess_primary;
    
    & .filter_icon{
       filter:  invert(22%) sepia(8%) saturate(9%) hue-rotate(5deg) brightness(90%) contrast(84%);
    } 
}

.container_icon {
    display: flex;
    gap: 1rem;
}

.col input {
    height: 50px;
    padding-left: 1rem;

}

button {
    width: 33%;
}

h4 {
    font-size: 18px;
}

.site_img {
    padding-bottom: 11rem;
}

.filter_icon {
    filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(103deg) brightness(105%) contrast(105%);
}

/* Button */
.bg_primary {
  background-color: $chess_primary;
  border: none;
}
.bg_primary:hover {
 background-color: $chess_secondary;
 color: $chess_primary;
 border: 1px solid $chess_white;
}
</style>