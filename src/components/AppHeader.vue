<script>
import AppNavbar from './AppNavbar.vue';

export default {
  name: 'AppHeader',
  data() {
    return {};
  },
  components: { AppNavbar }
}
</script>

<template>
  <section class="header">
    <AppNavbar />
    <h1>
      ciao
    </h1>

  </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

section.header {
  background-image: url('../assets/img/imagesZip/img-header/background-pattern-wavify.png');
  background-color: $color-6;
}
</style>
