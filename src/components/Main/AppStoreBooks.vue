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
                <h2 class="text-uppercase fs-6 mb-4">Book store online</h2>
                <p class="text-section-book">Be Alpha With <span class="color-2">Wingman's Book</span></p>
                <ul class="mb-5">
                    <li class="mb-2" v-for="opportunity in opportunityList" :key="opportunity">
                        <i class="color-2 fa-solid fa-check"></i>  {{ opportunity }}
                    </li>
                    <div class="pt-3">
                        <button class="started-button">
                            Get Free Ebooks
                        </button>
                    </div>
                </ul>
            </div>
            <!-- shop books -->
            <div class="col-7 d-flex">
                <article v-for="book in booksShop" :key="book" class="my_section-books position-relative">
                    <img class="card-img-top" :src="book.img" alt="">
                    <div class="card-body">
                        <h5 class="card-title text-center py-3 fs-6 fw-bold">{{ book.info }}</h5>
                        <p class="card-text text-center color-2 fw-bold fs-4">{{ book.price }}</p>
                    </div>
                    <div class="nav-shop">
                        <div class="container-icon text-center">
                            <i class="fa-solid fa-magnifying-glass"></i>
                        </div>
                        <div class="container-icon text-center">
                            <i class="fa-solid fa-cart-shopping"></i>
                        </div>
                        <div class="container-icon text-center">
                            <i class="fa-regular fa-heart"></i>
                        </div>
                        <div class="container-icon text-center">
                            <i class="fa-solid fa-signal"></i>
                        </div>
                    </div>
                </article>
            </div>
            <div class="col-2 logo-partners" v-for="partner in brandPartnersList" :key="partner">
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
        margin-bottom: 11rem
    }

    .my_section-books:hover .nav-shop {
        display: flex;
    }

    p.text-section-book {
        @include font (font-family);
        font-size: 3rem;
        line-height: 3.5rem;

    }

    .color-2 {
        color: $color-2
    }

    div.nav-shop {
        flex-direction: column;
        position: absolute;
        top: 50px;
        right: 30px;
        display: none;

        div.container-icon {
            background-color: $color-1;
            border-radius: 50%;
            width: 27px;
            height: 27px;
            margin-bottom: .7rem
        }

        i {
            font-size: .7rem;
        }

    }

    div.logo-partners {
        margin-bottom: 6rem
    }

    button.started-button {
        @include button-green(background-color, color, padding);
    }
}
</style>