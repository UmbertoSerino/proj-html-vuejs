<script setup>
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/Main/AppMain.vue';
import AppFooter from './components/Footer/AppFooter.vue';
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use '../node_modules/bootstrap/scss/bootstrap.scss' as*;
@use './style/general.scss' as*;
</style>
