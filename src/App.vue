<script>
import AppHeader from './components/AppHeader.vue'
import AppCard from './components/AppCard.vue'
import AppFooter from './components/AppFooter.vue'

export default {
    name: "Main",
    components: {
    AppHeader,
    AppCard,
    AppFooter,
},
};

</script>

<template>
    <!-- header -->
  <AppHeader />
  <!-- main -->
  <main>
    <div class="container">
        <div class="row-2 flex wrap gap-25">
            <AppCard/>
            <AppCard/>
            <AppCard/>
            <AppCard/>
            <AppCard/>
            <AppCard/>
        </div>
    </div>
  </main>
  <!-- footer -->
  <AppFooter />
</template>

<style>
</style>
