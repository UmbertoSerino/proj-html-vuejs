<script>
export default {
    name: 'AppAboutMe'
}
</script>
<template>
    <section class="my_wrapper">
        <div class="row">
            <h1 class="text-uppercase">About me</h1>
            <div class="col-4">
                <p class="my_playfair my_font-1">How to Be an Alpha Male: The 15 Habits of True Alphas</p>
            </div>
            <div class="offset-1 col-7 mb-5">
                <p class="my_font-2">Want to learn how to be <span class="text-green">an alpha male</span>? How to be more masculine?<br>
                    How to be the man you've always wanted to be?
                </p>
                <p>
                    Your goal is to show the consistency of business, core values, and customer care. Punsctuality, responsibility, accuracy, enthusiasm - you have to clearly explain
                    how these qualities are applicable to your work. And the important thing is you do love want you do.
                </p>
            </div>
        </div>
        <div class="row">
            <div class="col-6 position-relative mb-5">
                <img class="img-video" src="../../assets/img/imagesZip/img-main-aboutme/home-movation-video-poster-670x450.jpg" alt="alphaman picture">
                <img class="logo-youtube" src="../../assets/img/imagesZip/img-main-aboutme/icon-youtube-play.png" alt="">
            </div>
            <div class="col-4 info">
                <p class="my_playfair my_font-3 mb-5">
                    "Every morning you have two choices: continue to sleep with your dreams, or wake up and chase them."
                </p>
                <img class="mb-3" src="../../assets/img/imagesZip/img-main-aboutme/home-movation-shape-01.png" alt="">
                <h3 class="my_font">Kaixa Shark</h3>
                <p class="text-uppercase">Wingman</p>
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
        color: $color-2;
        font-size: 1rem;
        font-weight: 500;
        margin-bottom: 2rem;
    }

    p.my_playfair {
        @include font(font-family);

    }

    span.text-green {
        color: $color-2
    }

    ;

    div.info {
        padding: 2.3rem 0 0 3rem;
    }

    p.my_font-1 {
        font-size: 2.9rem;
        line-height: 3.5rem;
    }

    p.my_font-2 {
        font-size: 1.2rem;
        font-weight: 600;
    }

    p.my_font-3 {
        font-size: 1.7rem;
    }

    h3.my_font {
        font-size: 1.3rem;
        font-weight: 600;
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