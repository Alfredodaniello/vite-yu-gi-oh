<script>
import axios from 'axios';
import { store } from '../store.js';
export default {
    name: "AppSearch",
    data() {
        return {
            store
        };
    },
    methods: {
        getArchetypes() {
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {
                store.archetypes = response.data;
            })
        },
        resetFilter() {
            store.filter = "";
        },
    },
    
    mounted() {
        this.getArchetypes();
    }
}
</script>

<template>
<div class="top d-flex align-items-center general pt-3">
            <div class="select-container px-2 d-flex gap-3">
                <select class="form-select" aria-label="Default select example" v-model="store.filter" @change="$emit('filterCards')">
                    <option value="">Scegli l'archetipo!</option>
                    <option v-for="archetype in store.archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
                </select>
                <button @click="resetFilter()">Reset</button>
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