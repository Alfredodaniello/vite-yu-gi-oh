<script>
export default {
    name: "Cards"
}
</script>

<template>
<div class="card text-center">
    <div class="card-image">
        <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
    </div>
    <h5>ciao</h5>
    <span>ciao</span>
</div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card {
    color: white;
    width: calc(100% / 6);
    background-color: $brand-primary;
    .card-image {
        img{
            width: 100%;
        }
    }
}
</style>