<script>
import { store } from './../store'
export default {   
    data() {
        return {
            store
        }
    },
    
methods: {
    search(event){
    this.$emit('filter');
    }
},
}
</script>

<template>
    <select id="types" v-model="store.value" @change="search">
        <option value="" disabled selected>scegli l'archetipo</option>
        <option 
        v-for="arche in store.archeList"
        :value="arche.archetype_name"
        placeholder="scegli l'archetipo"
        >{{ arche.archetype_name }}</option>
    </select>
</template>

<style scoped>
    #types{
        margin: 20px 0;
        font-size: 25px;
        background-color: white;
    }
</style>