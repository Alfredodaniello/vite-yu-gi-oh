<script>
export default {
    name: "Cards",
    props: {
        cardsInfo : Object
    }
}
</script>

<template>
<div class="card-container pt-2">
    <div class="card text-center mb-3">
    <div class="card-image">
        <img :src="'https://images.ygoprodeck.com/images/cards/' + cardsInfo.id + '.jpg'" alt="">
    </div>
    <h5 class="pt-1">{{cardsInfo.name}}</h5>
    <span class="pb-1" v-if="cardsInfo.archetype">{{ cardsInfo.archetype }}</span>
</div>
</div>

</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card-container {
    width: calc((100% / 5) - 20px);
}
.card {
    color: white;;
    background-color: $brand-primary;
    .card-image {
        img{
            width: 100%;
        }
    }
}
</style>