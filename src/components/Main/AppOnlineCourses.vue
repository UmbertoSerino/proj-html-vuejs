<script>
export default {
    name: 'AppOnlineCourses',
    props: {
        latestCorses: {
            type: Array,
            required: true
        }
    },
    data() {
        return {
        }
    },
    methods: {

    },
}
</script>
<template >
    <section class="my_wrapper mb-5">
        <h1 class="text-uppercase text-center fs-5">Begin your journey at maxcoach</h1>
        <h2 class="text-center text-courses mb-5">Latest <span class="text-courses"> Online Couses</span>
        </h2>
        <div class="d-flex flex-wrap">
            <article v-for="courses in latestCorses" :key="courses" class="my_section-card">
                <img class="card-img-top" :src="courses.img" :alt="`${courses.alt}`">
                <div class="my_container-info-card">
                    <h5 class="card-title">{{ courses.price }}</h5>
                    <p class="fw-bold fs-5 card-text">{{ courses.info }}</p>
                    <div class="d-flex">
                        <p class="card-text pe-2"><small class="text-muted"><i class="pe-2 fa-solid fa-sheet-plastic"></i>{{ courses.lessons }} lessons</small></p>
                        <p class="card-text"><small class="text-muted"><i class="pe-2 fa-regular fa-user"></i>{{ courses.students }} students</small></p>
                    </div>
                </div>
            </article>
            <div class="w-100 text-center py-5">
                <button class="started-button fw-bold px-5">View all courses
                    <i class="fa-solid fa-arrow-right-long"></i>
                </button>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container(width, margin);

    article.my_section-card {
        width: calc((100% / 3) - 2rem);
        margin: 1rem;
    }

    h2.text-courses {
        @include font(font-family);
        font-size: 3.3rem;
    }

    span.text-courses {
        color: $color-2
    }

    h5 {
        padding-top: 1.5rem;
        padding-bottom: 1rem;
        color: $color-2;
        font-weight: 700
    }

    div.my_container-info-card {
        width: 80%;
        margin: 0 auto
    }

    button.started-button {
        @include button-green(background-color, color, padding);
    }
}
</style>