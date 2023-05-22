<script>
import AppCards from '../components/AppCards.vue';

export default{
    components: {
    AppCards,
	}
}
</script>

<template>
    <div class="container">
        <!-- TODO: add input component -->
        
        <div class="card-container" v-for="card in store.cardList" :key="card.id">
            <!-- TODO: add counter component -->

            <AppCards/>
        </div>

    </div>

</template>

<style scoped>
    .container{
        background-color:rgb(212, 143, 56) ;
        height: calc(100Vh - 200px);
    }
</style>