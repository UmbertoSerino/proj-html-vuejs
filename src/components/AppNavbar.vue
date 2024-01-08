<script>
import AppNavTools from './AppNavTools.vue';
import { store } from '../js/store';
export default {
    name: 'AppNavbar',
    data() {
        return {
            store,
            // creato un array di oggetti da inserire nella navbar, l'array contiene sia la parte name, che sara' visibile al click dell'utente e un items che sara' un array che conterra' tutti i link utili all'utente quando clicca sul name
            navList: [
                { name: 'Home', items: ['Home-link1', 'Home-link2', 'Home-link3', 'Home-link4'] },
                { name: 'Pages', items: ['Page1', 'Page2', 'Page3'] },
                { name: 'Courses', items: ['Courses1', 'Courses2', 'Courses3'] },
                { name: 'Features', items: ['Features1', 'Features2', 'Features3', 'Features4'] },
                { name: 'Blog', items: ['Blog1', 'Blog2', 'Blog3', 'Blog4'] },
                { name: 'Shop', items: ['Shop1', 'Shop2', 'Shop3', 'Shop4'] },
            ],
            isToolsActive: false,
        };
    },
    methods: {
        ToolsActive() {
            const tools = document.querySelector('ul.tools-list')
            if (this.isToolsActive == false) {
                tools.classList.add('tools-none')
            } else {
                tools.classList.add('tools-block')
            }
            this.isToolsActive = !this.isToolsActive;
        }
    },
    created() {

    },
    // ci creiamo un compoents, AppNavTools, che saranno i nostri tools che saranno visibili quando l'utente clicca sul link
    components: { AppNavTools }
}
</script>
<template>
    <section class="my_container">

        <nav class="d-flex justify-content-between align-items-center">
            <div class="logo-brand">
                <img src="../assets/img/imagesZip/img-header/dark-logo.png" alt="brand logo">
            </div>
            <div class="d-flex">
                <ul class="d-flex m-0" @click="ToolsActive()">
                    <!-- creiamo una lista ciclando nell'array navList -->
                    <li v-for="item in navList" :key="item" class="mx-2">
                        {{ item.name }}
                        <img class="arrow" src="../assets/img/imagesZip/img-header/image (1).png" alt="arrow down icons">
                        <img class="arrow d-none" src="../assets/img/imagesZip/img-header/image.png" alt="arrow up icons">
                        <!-- inviamo i dati item al component AppNavTools -->
                        <div>
                            <ul class="tools-list tools-none" v-if="item.items">
                                <li v-for="subItem in item.items" :key="subItem">{{ subItem }}
                                </li>
                            </ul>
                        </div>
                    </li>
                </ul>
            </div>
            <div>
                <!-- qui andranno inserite le icon per l'indirizzamento ai profili social -->
                <span>X</span>
                <span>F</span>
                <span>I</span>
                <span>L</span>
            </div>
        </nav>
    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

section.my_container {
    @include container(width, margin);

    nav {
        height: 50px;

        .logo-brand {
            height: 100%;

            img {
                height: 100%;
                padding: 1rem;
            }
        }
    }

    li {
        border-bottom: 1px solid transparent;
    }

    li:hover {
        color: $color-2;
        border-bottom: 1px solid $color-2;
    }

    ul.tools-list {
        position: absolute;
    }

    ul.tools-none {
        display: none;
    }

    ul.tools-block {
        display: block;
    }
}
</style>
