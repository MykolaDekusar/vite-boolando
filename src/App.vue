<script>
import AppHeader from './components/AppHeader.vue'
import MainContainer from './components/MainContainer.vue'
import AppFooter from './components/AppFooter.vue'

export default {
    name: "Main",
    components: {
        AppHeader,
        MainContainer,
        AppFooter,
    },
};

</script>

<template>
  <!-- header -->
  <AppHeader />
  <!-- main -->
  <MainContainer/>
  <!-- footer -->
  <AppFooter />
</template>

<style>
</style>
