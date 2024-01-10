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
    <section class="my_wrapper">
        <h1 class="fs-6 mb-5 text-uppercase">Blog Updated</h1>
        <p class="text-courses mb-5">
            Interesting <span class="color-2">articles updated</span> daily
        </p>
        <div class="d-flex">
            <article v-for="article in articlesInteresting" :key="article" class="my_section-card">
                <img class="card-img-top" :src="article.picture" alt="">
                <div>
                    <p class="card-text pe-2 pt-3"><small class="text-muted"><i class="fa-regular fa-clipboard me-2"></i>{{ article.date }}</small></p>
                    <h5 class="my_title font-weight-bold mb-3">{{ article.title }}</h5>
                    <p class="card-text">{{ article.info }}</p>
                    <div class="d-flex">
                    </div>
                </div>
            </article>
        </div>
        <div class="text-center">
            <span class="view-all-posts text-uppercase" href="">view all posts</span>
        </div>
    </section>

</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container (width, margin);
    margin-bottom: 8rem;

    p.text-courses {
        @include font(font-family);
        font-size: 3.3rem;
    }

    h5.my_title {
        font-weight: 600;
        line-height: 1.8rem;
    }

    .color-2 {
        color: $color-2
    }

    span.view-all-posts {
        color: $color-2;
        line-height: 1rem;
        border-bottom: 1px solid $color-2;
        font-size: 1rem;
        font-weight: 600;

    }

    article.my_section-card {
        width: calc((100% / 3) - 2rem);
        margin: 1rem;
        margin-bottom: 3rem;
    }
}
</style>