<script>
import AppNavbar from './AppNavbar.vue';
import AppJumbotron from './AppJumbotron.vue';

export default {
  name: 'AppHeader',
  data() {
    return {};
  },
  components: {
    AppNavbar,
    AppJumbotron
  },

}
</script>

<template>
  <header>

    <AppNavbar />
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
