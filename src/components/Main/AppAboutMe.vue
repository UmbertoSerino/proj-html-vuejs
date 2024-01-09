<script>
export default {
    name: 'AppAboutMe'
}
</script>
<template lang="">
    <section class="my_wrapper">
        <div class="row">
            <div class="col-5">
                <h1>About me</h1>
                <p>How to Be an Alpha Male: The 15 Habitats of True Alphas</p>
            </div>
            <div class="col-7">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum excepturi culpa eveniet dicta quasi co
                </p>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti eaque rerum inventore ullam, reiciendis porro voluptatibus fugiat molestias enim debitis culpa sit aut obcaecati saepe facere, dolor ducimus! Nemo, doloribus.
                </p>
            </div>
        </div>
        <div class="row">
            <div class="col-6 position-relative">
                <img class="img-video" src="../../assets/img/imagesZip/img-main-aboutme/home-movation-video-poster-670x450.jpg" alt="alphaman picture">
                <img class="logo-youtube" src="../../assets/img/imagesZip/img-main-aboutme/icon-youtube-play.png" alt="">
            </div>
            <div class="col-6 py-5">
                <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, provident recusandae ut voluptatibus e
                </p>
                <img src="../../assets/img/imagesZip/img-main-aboutme/home-movation-shape-01.png" alt="">
                <p>Kaixa Shark</p>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container(width, margin);

    h1 {
        color: $color-2
    }

    .img-video {
        width: 100%;
    }

    img.logo-youtube {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        width: 15%;
    }
}
</style>