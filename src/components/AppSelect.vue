<script>
// import { store } from './../store'
export default {   
methods: {
    // emitFilter(){
    //     this.$emit('filter', this.event.target.value)
    // }
},
}
</script>

<template>
    <select name="types" id="types" @change="$emit('filter')">
        <option value="Alien">Alien</option>
        <option value="Noble Knight">Noble Knight</option>
        <option value="Melodious">Melodious</option>
    </select>
</template>

<style scoped>
    #types{
        margin: 20px 0;
        font-size: 25px;
        background-color: white;
    }
</style>