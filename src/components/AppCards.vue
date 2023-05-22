<script>
export default {   

    props: {
        cardsData: Object,
    }
}

</script>

<template>
    <div class="card">
        <img :src="cardsData.card_images[0].image_url" alt="">
        <div class="name">{{ cardsData.name }}</div>
        <div class="archetype">{{ cardsData.archetype }}</div>
    </div>
</template>

<style scoped>
.card{
    margin: 20px;
    display: flex;
    flex-direction: column;
}

.name,.archetype{
    background-color: rgb(212, 143, 56);
    padding: 10px;
}
    
img{
    height: 300px;
}

</style>