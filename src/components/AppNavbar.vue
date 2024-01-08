<script>

export default {
    name: 'AppNavbar',
    data() {
        return {
            navList: [
                { name: 'Home', items: ['Home-link1', 'Home-link2', 'Home-link3', 'Home-link4'] },
                { name: 'Pages', items: ['Page1', 'Page2', 'Page3'] },
                { name: 'Courses', items: ['Courses1', 'Courses2', 'Courses3'] },
                { name: 'Features', items: ['Features1', 'Features2', 'Features3', 'Features4'] },
                { name: 'Blog', items: ['Blog1', 'Blog2', 'Blog3', 'Blog4'] },
                { name: 'Shop', items: ['Shop1', 'Shop2', 'Shop3', 'Shop4'] },
            ],
        };
    },

}
</script>
<template>
    <div class="container">
        <nav class="navbar">
            <div class="navbar-brand">
                <img src="../assets/img/imagesZip/img-header/dark-logo.png" alt="">
            </div>
            <div class="d-flex">
                <ul class="d-flex">
                    <li v-for="item in navList" :key="item" class="mx-2">
                        {{ item.name }}
                    </li>
                </ul>
            </div>
            <div>
                <span>X</span>
                <span>F</span>
                <span>I</span>
                <span>L</span>

            </div>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

ul {
    list-style-type: none;
}
</style>
