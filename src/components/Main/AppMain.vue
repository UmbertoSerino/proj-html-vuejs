<script>
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
}
</script>
<template>
    <main>
        <h1>main</h1>
        <div class="d-flex justify-content-center">
            <section class="value-course mx-5" v-for="statistic in courseStatistics" :key="statistic">
                <p class="value-date fs-3 text-center">{{ statistic.data }}</p>
                <p class="value-info text-uppercase">{{ statistic.name }}</p>
            </section>

        </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

main {
    @include container (width, margin)
}

section.value-course {
    .value-date {
        color: $color-2
    }

    .value-info {
        font-size: .7rem;
    }

}
</style>