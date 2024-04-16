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
            <div class="select-container px-2">
                <select class="form-select" aria-label="Default select example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                </select>
            </div>
        </div>
        <div class="d-flex flex-wrap justify-content-between">
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

.select-container {
    width: 30%;
}

</style>