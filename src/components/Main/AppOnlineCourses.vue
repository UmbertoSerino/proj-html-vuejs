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
        <div class="d-flex flex-wrap">
            <div v-for="courses in latestCorses" :key="courses" class="my_section-card card">
                <img class="card-img-top" :src="courses.img" :alt="`${courses.alt}`">
                <div class="card-body">
                    <h5 class="card-title">{{ courses.price }}</h5>
                    <p class="card-text">{{ courses.info }}</p>
                    <div class="d-flex">
                        <p class="card-text pe-2"><small class="text-muted">{{ courses.lessons }} lessons</small></p>
                        <p class="card-text"><small class="text-muted">{{ courses.students }} students</small></p>
                    </div>
                </div>
            </div>
            <div class="w-100 text-center">
                <button class="started-button">View all courses
                    <i class="fa-solid fa-arrow-right-long"></i>
                </button>
            </div>
        </div>
    </section>
</template>
<style lang="scss">
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container(width, margin);

    div.my_section-card {
        width: calc((100% / 3) - 2rem);
        margin: 1rem;
    }

    button.started-button {
        @include button-green(background-color, color, padding);
    }
}
</style>