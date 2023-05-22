<script>
export default {   

    props: {
        cardsData: Object,
    }
}

</script>

<template>
    <div class="card">
        <img :src="cardsData.card_images.image_url" alt="">
        <div class="name">{{ cardsData.name }}</div>
        <div class="archetype">{{ cardsData.archetype }}</div>
    </div>
</template>

<style>
    
</style>