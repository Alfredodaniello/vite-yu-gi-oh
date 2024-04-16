<script>
export default {
    name: "Cards",
    props: {
        cardsInfo : Object
    }
}
</script>

<template>
<div class="card text-center mb-3">
    <div class="card-image">
        <img :src="'https://images.ygoprodeck.com/images/cards/' + cardsInfo.id + '.jpg'" alt="">
    </div>
    <h5 class="pt-1">{{cardsInfo.name}}</h5>
    <span class="pb-1" v-if="cardsInfo.archetype">{{ cardsInfo.archetype }}</span>
</div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card {
    color: white;
    width: calc(100% / 5 - 30px);
    background-color: $brand-primary;
    .card-image {
        img{
            width: 100%;
        }
    }
}
</style>