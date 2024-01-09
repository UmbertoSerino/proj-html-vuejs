<script>
import AppAboutMe from './AppAboutMe.vue';
export default {
    name: 'AppMain',
    data() {
        return {
            courseStatistics: [
                { name: 'Finished Season', data: '1.926' },
                { name: 'Satisfaction rate', data: '100%' },
                { name: 'Enrolled Learners', data: '3092+' },
                { name: 'Online Instructors', data: 200 }],
        }
    },
    components: {
        AppAboutMe
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