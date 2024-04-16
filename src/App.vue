<script>
import { store } from './store.js';
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import Cards from './components/Cards.vue';
import CardsContainer from './components/CardsContainer.vue';
import AppLoader from './components/AppLoader.vue';
import AppSearch from './components/AppSearch.vue';
export default {
    components: {
        AppHeader,
        Cards,
        CardsContainer,
        AppLoader,
        AppSearch
    },
    data(){
        return{
            store
        }
    },
    methods: {
        getCardsFromApi(){
            const queryParams = {
                num: 20,
                offset: 0,
            };
            axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php", {
                params: queryParams
            })
            .then((response) => {
                store.card = response.data.data;
                store.loading = false;
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
    <AppSearch></AppSearch>
    <CardsContainer v-if="store.loading === false"></CardsContainer>
    <AppLoader v-else></AppLoader>
</main>
    

</template>

<style lang="scss">
@use "./style/partials/generic" as *;
@use "./style/partials/variables" as *;
</style>