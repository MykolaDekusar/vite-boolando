<script>
import AppCard from './AppCard.vue'
export default {
    name:"Main Container",
    components: {
        AppCard,
    }
}
</script>

<template>
<main>
    <div class="container">
        <div class="row-2 flex wrap gap-25">
            <AppCard />
        </div>
    </div>
  </main>
</template>

<style scoped>
main {
    margin-top: 48.66px;
    padding: 50px 0;
}
</style>