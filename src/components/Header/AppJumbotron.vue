<script>
export default {
    name: 'AppJumbotron',
    data() {
        return {
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
            <div class="col-5 my_min-width py-5">
                <h1 class="fs-6 text-uppercase mb-4">I'm Wigman</h1>
                <h2 class="my_playfair">Peace On Earth A Wonderful Wish But No Way</h2>
                <h3 class="my_font">Success isn't avernight. It's when everyday you get a little better than the day before. It all adds up</h3>
                <button class="started-button fw-bold my_font">Get a Started For Free
                    <i class="fa-solid fa-arrow-right-long"></i>
                </button>
            </div>
            <div class="offset-1 col-6">
                <div class="my_bg-img">
                    <img src="../../assets/img/imagesZip/img-header/home-movation-hero-image.png" alt="">
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
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;


section.my_container {
    @include container(width, margin);
    background-image: url('../../assets/img/imagesZip/img-header/home-movation-shape-face-300x267.png');
    background-position: right;
    background-position-y: 150px;
    background-size: 450px;
    background-repeat: no-repeat;
    margin-bottom: 4rem;

    .my_bg-img {

        img {
            width: 80%;
            height: 100%;
        }
    }
}

h2.my_playfair {
    @include font(font-family);
    font-size: 3.38rem;
}

h3.my_font {
    font-size: .9rem;
    line-height: 1.7rem;
    margin-bottom: 2rem;
}

button.started-button {
    @include button-green(background-color, color, padding);
}

div.shop {
    position: fixed;
    z-index: 1;
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
