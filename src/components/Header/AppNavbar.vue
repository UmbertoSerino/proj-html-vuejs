<script>
export default {
    name: 'AppNavbar',
    data() {
        return {
            // creato un array di oggetti da inserire nella navbar, l'array contiene sia la parte name, che sara' visibile al click dell'utente e un items che sara' un array che conterra' tutti i link utili all'utente quando clicca sul name
            navList: [
                { name: 'Home', items: ['HomeLink-1', 'HomeLink-2', 'HomeLink-3', 'HomeLink-4'] },
                { name: 'Pages', items: ['Page-1', 'Page-2', 'Page-3'] },
                { name: 'Courses', items: ['Courses-1', 'Courses-2', 'Courses-3'] },
                { name: 'Features', items: ['Features-1', 'Features-2', 'Features-3', 'Features-4'] },
                { name: 'Blog', items: ['Blog-1', 'Blog-2', 'Blog-3', 'Blog-4'] },
                { name: 'Shop', items: ['Shop-1', 'Shop-2', 'Shop-3', 'Shop-4'] },
            ],
            // creiamo un indice che di base è false, in modo che al click cambi la sua proprieta' in modo da nascondere la finestra dei link
            activeIndex: false
        };
    },
    methods: {
        toolsActive(index) {
            if (this.activeIndex === index) {
                this.activeIndex = true;
            } else {
                this.activeIndex = index;
            }
        },

    },
    created() {

    },

}
</script>
<template>
    <section class="my_container">
        <nav class="d-flex justify-content-between align-items-center">
            <div class="logo-brand">
                <img src="../assets/img/imagesZip/img-header/dark-logo.png" alt="brand logo">
            </div>
            <div class="d-flex">
                <ul class="d-flex m-0 ">
                    <!-- creiamo una lista ciclando nell'array navList, la freccia di fianco ruota di 180deg ad ogni click -->
                    <li v-for="(item, index) in navList" :key="item" class="link mx-3 fw-bold" @click="toolsActive(index)">
                        {{ item.name }}
                        <img class="arrow" :class="{ 'arrow-rotate': activeIndex === index }" src=".././../assets/img/imagesZip/img-header/image (1).png" alt="arrow down icons">
                        <div class="tool">
                            <!-- al click viene aperta una finesta con i link utili, in base all'indice attivo -->
                            <ul class="tools-list tools-none" :class="{ 'tools-block': activeIndex === index }" v-if="item.items && activeIndex === index">
                                <li v-for="subItem in item.items" :key="subItem">{{ subItem }}
                                </li>
                            </ul>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="reference">
                <!-- qui andranno inserite le icon per l'indirizzamento ai profili social -->
                <a href="www.tweeter.com"><i class="fa-brands fa-twitter"></i></a>
                <a href=""><i class="fa-brands fa-facebook-f"></i></a>
                <a href=""><i class="fa-brands fa-instagram"></i></a>
                <a href=""><i class="fa-brands fa-linkedin"></i></a>
            </div>
        </nav>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

section.my_container {
    @include container(width, margin);
    padding: 1rem 0;
    margin-bottom: 2rem;

    nav {
        height: 50px;

        .logo-brand {
            height: 100%;

            img {
                height: 100%;
                padding: 1rem 0;
            }
        }
    }

    li.link {
        border-bottom: 1px solid transparent;
        position: relative;
    }

    li.link:hover {
        color: $color-2;
        border-bottom: 1px solid $color-2;
        cursor: pointer;
    }

    ul.tools-list {
        position: absolute;
        right: 0;
        background-color: $color-1 ;
        padding: .5rem 1rem .5rem 1rem;

        li {
            line-height: 2rem;
            color: black;
        }
    }

    ul.tools-none {
        display: none;
    }

    ul.tools-block {
        display: block;
    }

    img.arrow-rotate {
        transform: rotate(180deg);
    }

    div.reference {
        min-width: 120px;

        a {
            margin-right: 1rem;
            color: black;
        }
    }
}
</style>
