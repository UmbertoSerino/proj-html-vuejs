<script>
export default {
    name: 'AppStoreBooks',
    props: {
        booksShop: {
            type: Array,
            required: true
        },
        opportunityList: {
            type: Array,
            required: true
        },
        brandPartnersList: {
            type: Array,
            required: true
        }
    },
    data() {
        return {
        }
    },
    methods: {

    }
}
</script>
<template lang="">
    <section class="my_wrapper mb-5">
        <div class="row">
            <div class="col-5">
                <!-- opportunity list -->
                <h2 class="text-uppercase">Book store online</h2>
                <p>Be Alpha With Wingman's Book</p>
                <ul>
                    <li v-for="opportunity in opportunityList" :key="opportunity">
                        {{ opportunity }}
                    </li>
                </ul>
                <div>
                    <button class="started-button">
                        Get Free Ebooks
                    </button>
                </div>
            </div>
            <!-- shop books -->
            <div class="col-7 d-flex">
                <article v-for="book in booksShop" :key="book" class="my_section-books card position-relative">
                    <img class="card-img-top" :src="book.img" alt="">
                    <div class="card-body">
                        <h5 class="card-title text-center">{{ book.info }}</h5>
                        <p class="card-text text-center">{{ book.price }}</p>
                    </div>
                    <div class="nav-shop">
                        <i class="fa-solid fa-magnifying-glass"></i>
                        <i class="fa-solid fa-cart-shopping"></i>
                        <i class="fa-regular fa-heart"></i>
                        <i class="fa-solid fa-signal"></i>
                    </div>
                </article>
            </div>
            <div class="col-2" v-for="partner in brandPartnersList" :key="partner">
                <img :src="partner" alt="">
            </div>

        </div>
    </section>
</template>
<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container (width, margin);

    article.my_section-books {
        width: calc((100% / 2) - 2rem);
        margin: 1rem;
    }

    .my_section-books:hover .nav-shop {
        display: flex;
    }

    div.nav-shop {
        background-color: $color-1;
        flex-direction: column;
        position: absolute;
        top: 30px;
        right: 0;
        padding: .7rem;
        display: none;

        i {
            margin: 1rem 0
        }
    }

    button.started-button {
        @include button-green(background-color, color, padding);
    }
}
</style>