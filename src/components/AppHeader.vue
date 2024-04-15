<script>
export default {
    name: "AppHeader"
}
</script>

<template>
<div class="header d-flex align-items-center py-2">
    <div class="logo-container mx-2">
        <img src="../assets/img/logo.webp" alt="">
    </div>
    <h1>Yu-Gi-Oh API</h1>

</div>
</template>

<style scoped lang="scss">
.header {
    height: 70px;
    .logo-container {
        width: 150px;
        height: 100%;
        img {
            width: 100%;
            height: 100%;
        }
    }
}
</style>