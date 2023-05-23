<script>
export default {   
}
</script>

<template>
    <select name="types" id="types" @change="$emit('filter', event.target.value)">
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