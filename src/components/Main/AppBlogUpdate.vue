<script>
export default {
    name: 'AppBlogUpdate',
    props: {
        articlesInteresting: {
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
<template lang="">
    <section class="my_wrapper mb-5">
        <h1>Blog Updated</h1>
        <p>
            Interesting articles updated daily
        </p>
        <div class="d-flex">
            <article v-for="article in articlesInteresting" :key="article" class="my_section-card card">
                <img class="card-img-top" :src="article.picture" alt="">
                <div class="card-body">
                    <p class="card-text pe-2"><small class="text-muted">{{ article.date }}</small></p>
                    <h5 class="card-title">{{ article.title }}</h5>
                    <p class="card-text">{{ article.info }}</p>
                    <div class="d-flex">
                    </div>
                </div>
            </article>
        </div>
        <div class="text-center">
            <a href="">view all posts</a>
        </div>
    </section>

</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container (width, margin);

    article.my_section-card {
        width: calc((100% / 3) - 2rem);
        margin: 1rem;
    }
}
</style>