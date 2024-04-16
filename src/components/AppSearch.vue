<script>
export default {
    name: "AppSearch"
}
</script>

<template>
<div class="top d-flex align-items-center general pt-3">
            <div class="select-container px-2">
                <select class="form-select" aria-label="Default select example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                </select>
            </div>
        </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.select-container{
    width: 1200px;
    margin: auto;
    .form-select{
        width: 20%;
    }
}

.general {
    background-color: $brand-primary;
}


</style>