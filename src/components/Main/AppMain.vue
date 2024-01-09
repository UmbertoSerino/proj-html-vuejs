<script>
import AppAboutMe from './AppAboutMe.vue';
import AppOnlineCourses from './AppOnlineCourses.vue';
export default {
    name: 'AppMain',
    data() {
        return {
            // creato un array per inserire i dati del corso attuali
            courseStatistics: [
                { name: 'Finished Season', data: '1.926' },
                { name: 'Satisfaction rate', data: '100%' },
                { name: 'Enrolled Learners', data: '3092+' },
                { name: 'Online Instructors', data: 200 }],
            latestCorses: [
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-01-480x298.jpg", alt: "picture 2 man with pc", price: "$30.00", info: "How to be Successful:Create A Growth Mindset For Success", lessons: "3", students: "50" },
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-02-480x298.jpg", alt: "picture teacher with students", price: "$30.00", info: "How to Build Confidence in Your Abilities", lessons: "1", students: "50" },
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-03-480x298.jpg", alt: "picture another 2 man with pc", price: "$20.00", info: "Productivity Machine - Focus in a Distracted World", lessons: "5", students: "50" },
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-04-480x298.jpg", alt: "man with pc", price: "$20.00", info: "Effective Time Management Mastery - Complete Guide", lessons: "18", students: "50" },
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-05-480x298.jpg", alt: "picture alphaman drinking", price: "$25.99", info: "Body Language Secrets for Entrepreneurs", lessons: "18", students: "50" },
                { img: "../../assets/img/imagesZip/img-main-latest-courses/motivation-course-06-480x298.jpg", alt: "picture alphaman calling", price: "$19.99", info: "Management Skills: The Science od Leadership", lessons: "17", students: "50" }]
        }
    },
    components: {
        AppAboutMe,
        AppOnlineCourses
    }
}
</script>
<template>
    <main>
        <div class="my_wrapper d-flex justify-content-center">
            <section class="value-course mx-5" v-for="statistic in courseStatistics" :key="statistic">
                <p class="value-date fs-3 text-center">{{ statistic.data }}</p>
                <p class="value-info text-uppercase">{{ statistic.name }}</p>
            </section>
        </div>
        <AppAboutMe />
        <AppOnlineCourses :latestCorses="latestCorses" />
    </main>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

div.my_wrapper {
    @include container (width, margin);
    margin-bottom: 3rem;

    section.value-course {

        .value-date {
            color: $color-2
        }

        .value-info {
            font-size: .7rem;
        }

    }

}
</style>