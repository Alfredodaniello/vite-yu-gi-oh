<script>
import { store } from '../store.js';
import Cards from './Cards.vue';
export default {
    components: {
        Cards
    },
    data() {
        return {
            store
        }
    },
    name: "CardsContainer"
}
</script>

<template>
<div class="ms-container top"></div>
<div class="ms-container d-flex flex-wrap">
    <Cards v-for="card in store.card"></Cards>
</div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.top {
    height: 70px;
    background-color: black;
}
.ms-container{
    width: 1200px;
    margin: auto;
}

</style>