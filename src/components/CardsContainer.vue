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
<div class="general pt-5">
    <div class="ms-container p-5">
        <div class="top d-flex align-items-center">
        </div>
        <div class="d-flex flex-wrap card-container">
            <Cards v-for="card, index in store.card" :key="card.id" :cardsInfo="card"></Cards>
        </div>
    </div>
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
    background-color: white;
}

.general {
    background-color: $brand-primary;
}

.card-container {
    gap: calc(25px)
}


</style>