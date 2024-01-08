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
  <AppNavbar />
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;
</style>
