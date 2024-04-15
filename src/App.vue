<script>
import { store } from './store.js';
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
    data(){
        return{
            store
        }
    },
    methods: {
        getCardsFromApi(){
            axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
            .then((response) => {
                store.card = response.data.data
            })
            
        },
    },
    mounted(){
        this.getCardsFromApi();
    }
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