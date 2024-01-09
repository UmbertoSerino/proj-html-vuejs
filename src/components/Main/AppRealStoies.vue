<script>
export default {
    name: 'AppRealStories',
    props: {
        testimonials: {
            type: Array,
            required: true
        }
    },
    data() {
        return {

        }
    },
}
</script>
<template>
    <section class="container-fluid position-relative">
        <div class="row">
            <div class="col-6 my_background text-center">
                <h1>real stories</h1>
                <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente doloribus id incidunt, iusto perferendis libero, vel alias consequatur exercitationem odit
                    excepturi minus, sequi accusamus vitae officiis. Vel vitae excepturi fugit? </p>
                <div class="picture-testimonails">
                    <img src="../../../public/img-main-real-stories/testimonial-avata-02.jpg" alt="">
                </div>
            </div>
            <div class="col-6 p-0">
                <img class="picture-alphaman" src="../../assets/img/imagesZip/img-main-real-stories/home-movation-testimonial-image-768x562.jpg" alt="picture alphaman">
            </div>
        </div>
        <div class="carousel-control">
            <div class="text-center p-0">
                <img src="../../assets/img/imagesZip/img-header/image.png" alt="arrow-up">
            </div>
            <div class="text-center">
                <span>1/4</span>
            </div>
            <div class="text-center">
                <img src="../../assets/img/imagesZip/img-header/image (1).png" alt="arrow-down">
            </div>
        </div>

    </section>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

.my_background {
    background-image: url('../../assets/img/imagesZip/background-pattern-wavify.png');
    background-color: $color-6;
    display: flex;
    flex-direction: column;
    align-items: center;
}

div.carousel-control {
    width: 70px;
    border-radius: 50%;
    position: absolute;
    top: 50%;
    right: 50%;
    transform: translate(50%, -50%);
    background-color: $color-1;
}

div.picture-testimonails {
    width: 70px;

    img {
        border-radius: 50%;
        width: 100%;
    }
}

img.picture-alphaman {
    width: 100%;
}
</style>