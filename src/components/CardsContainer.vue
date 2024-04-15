<script>
import Cards from './Cards.vue';
export default {
    components: {
        Cards
    },
    name: "CardsContainer"
}
</script>

<template>
<div class="ms-container top"></div>
<div class="ms-container">
    <Cards></Cards>
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