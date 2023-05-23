<script>
import { store } from './../store'
export default {   
    data() {
        return {
            store
        }
    },
    
methods: {
    // emitFilter(){
    //     this.$emit('filter', this.event.target.value)
    // }
},
}
</script>

<template>
    <select name="types" id="types" @change="$emit('filter', event.target.value)" v-model="store.archeList">
        <option v-for="arche in store.archeList">{{ arche.archetype_name }}</option>
    </select>
</template>

<style scoped>
    #types{
        margin: 20px 0;
        font-size: 25px;
        background-color: white;
    }
</style>