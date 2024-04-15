<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import Cards from './components/Cards.vue';
export default {
    components: {
        AppHeader,
        Cards
    },
}
</script>

<template>
<header>
    <AppHeader></AppHeader>
</header>
<main>
    <Cards></Cards>
</main>
    

</template>

<style lang="scss">
@use "./style/partials/generic" as *;
@use "./style/partials/variables" as *;
</style>