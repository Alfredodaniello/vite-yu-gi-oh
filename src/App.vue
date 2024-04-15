<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import Cards from './components/Cards.vue';
import CardsContainer from './components/CardsContainer.vue';
export default {
    components: {
        AppHeader,
        Cards,
        CardsContainer
    },
}
</script>

<template>
<header>
    <AppHeader></AppHeader>
</header>
<main>
    <CardsContainer></CardsContainer>
</main>
    

</template>

<style lang="scss">
@use "./style/partials/generic" as *;
@use "./style/partials/variables" as *;
</style>