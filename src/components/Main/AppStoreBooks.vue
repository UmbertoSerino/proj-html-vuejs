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
        }
    },
    data() {
        return {
        }
    },
    methods: {
        logImagePath(imagePath) {
            console.log('Percorso dell\'immagine:', imagePath);
        }
    }
}
</script>
<template lang="">
    <section class="my_wrapper mb-5">
        <div class="row">
            <div class="col-5">
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
            <div class="col-7 d-flex">
                <div v-for="book in booksShop" :key="book" class="my_section-books card">
                    <img class="card-img-top" :src="book.img" alt="">
                    <div class="card-body">
                        <h5 class="card-title text-center">{{ book.info }}</h5>
                        <p class="card-text text-center">{{ book.price }}</p>
                    </div>
                </div>
            </div>
            <div class="col-2">
                <img src="" alt="">
            </div>
            <div class="col-2">aaa</div>

        </div>
    </section>
</template>
<style lang="scss">
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_wrapper {
    @include container (width, margin);

    div.my_section-books {
        width: calc((100% / 2) - 2rem);
        margin: 1rem;
    }

    button.started-button {
        @include button-green(background-color, color, padding);
    }
}
</style>