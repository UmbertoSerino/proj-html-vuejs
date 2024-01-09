<script>
import AppNavbar from './AppNavbar.vue';
import AppJumbotron from './AppJumbotron.vue';

export default {
  name: 'AppHeader',
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
    };
  },
  components: {
    AppNavbar,
    AppJumbotron
  },

}
</script>

<template>
  <header>
    <!-- inviamo l'array da iterare all'AppNavbar -->
    <AppNavbar :navList="navList" />
    <AppJumbotron />

  </header>
</template>

<style lang="scss" scoped>
@use '../../style/partials/mixins' as*;
@use '../../style/partials/variables' as*;

header {
  background-image: url('../../assets/img/imagesZip/img-header/background-pattern-wavify.png');
  background-color: $color-6;
}
</style>
