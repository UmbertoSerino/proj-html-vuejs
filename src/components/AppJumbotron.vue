<script>
import { store } from '../js/store';
export default {
    name: 'AppJumbotron',
    data() {
        return {
            store,
        };
    },
    methods: {

    },
    created() {

    },

}
</script>
<template>
    <section class="my_container">
        <div class="row">
            <div class="col-6 my_min-width">
                <h1 class="fs-5 text-uppercase">I'm Wigman</h1>
                <h2>Peace On Earth A Wonderful Wish But No Way</h2>
                <h3 class="fs-5">Success isn't avernight. It's when everyday you get a little better than the day before. It all adds up</h3>
                <button class="started-button">Get a Started For Free
                    <i class="fa-solid fa-arrow-right-long"></i>
                </button>
            </div>
            <div class="col-6">
                <div class="my_bg-img">
                    <img src="../assets/img/imagesZip/img-header/home-movation-hero-image.png" alt="">
                </div>
            </div>

        </div>
    </section>
    <div>
        <div class="shop d-flex flex-column justify-content-center">
            <i class="fa-brands fa-shopware"></i>
            <i class="fa-solid fa-store"></i>
            <i class="fa-solid fa-bell"></i>
            <i class="fa-solid fa-cart-shopping"></i>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;


section.my_container {
    @include container(width, margin);
    background-image: url('../assets/img/imagesZip/img-header/home-movation-shape-face-300x267.png');
    background-position: right;
    background-position-y: 200px;
    background-size: 550px;
    background-repeat: no-repeat;

    .started-button {
        background-color: $color-2;
        color: $color-1;
        padding: .7rem 2.5rem;
    }

    .my_bg-img {


        img {
            width: 90%;
            height: 100%;
        }
    }
}

div.shop {
    position: fixed;
    right: 0;
    top: 20%;
    background-color: white;
    border-radius: 3px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

    i {
        padding: 1rem .5rem;
    }
}
</style>
