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
            activeIndex: 0,
        }
    },
    methods: {
        nextTestimonial() {
            this.activeIndex = (this.activeIndex + 1) % this.testimonials.length
        },
        prevTestimonial() {
            this.activeIndex = (this.activeIndex - 1 + this.testimonials.length) % this.testimonials.length;
        }
    },
}
</script>
<template>
    <section class="my_wrapper-real-stories my_background position-relative">
        <div class="container-fluid">
            <div class="row">
                <div class="col-md-6">
                    <div class="container-testimonials text-center">
                        <h1 class="color-2 fs-6 fw-bold mb-5 text-uppercase">real stories</h1>
                        <p class="testimonial-info">{{ testimonials[activeIndex].info }}</p>
                        <div class="picture-testimonials">
                            <img :src="testimonials[activeIndex].img" alt="" />
                        </div>
                        <div class="mb-3">
                            <span class="fs-5">{{ testimonials[activeIndex].name }}</span>
                        </div>
                        <div>
                            <span>/ {{ testimonials[activeIndex].work }}</span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 p-0">
                    <img class="picture-alphaman" src="../../../public/img-main-real-stories/home-movation-testimonial-image-768x562.jpg" alt="picture alphaman" />
                </div>
            </div>
        </div>
        <div class="carousel-control">
            <div class="text-center p-0 arrow-up" @click="prevTestimonial">
                <img src="../../assets/img/imagesZip/img-header/image.png" alt="arrow-up">
            </div>
            <div class="text-center">
                <span>{{ activeIndex + 1 }}/{{ testimonials.length }}</span>
            </div>
            <div class="text-center arrow-down" @click="nextTestimonial">
                <img src="../../assets/img/imagesZip/img-header/image (1).png" alt="arrow-down">
            </div>
        </div>
    </section>
</template>
  
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;


section.my_wrapper-real-stories {
    min-width: 1220px;
    margin-bottom: 8rem;
}

.my_background {
    background-image: url('../../assets/img/imagesZip/background-pattern-wavify.png');
    background-color: $color-6;
    display: flex;
    flex-direction: column;
    align-items: center;
}

div.container-testimonials {
    padding-top: 5rem;
    width: 60%;
    max-width: 800px;
    margin: 0 auto;

    .color-2 {
        color: $color-2
    }

    p.testimonial-info {
        font-size: 1.44rem;
        line-height: 1.9rem;
        margin-bottom: 3rem
    }

    div.picture-testimonials {
        width: 90px;
        margin: 0 auto;
        margin-bottom: 2rem;

        img {
            border-radius: 50%;
            width: 100%;
        }
    }

}

div.container-alphaman {
    width: 50%;
}

img.picture-alphaman {
    width: 100%;
}

div.carousel-control {
    width: 75px;
    height: 75px;
    border-radius: 50%;
    position: absolute;
    top: 50%;
    right: 50%;
    transform: translate(50%, -50%);
    background-color: $color-1;
}
</style>