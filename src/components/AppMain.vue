<script>
import AppCards from './AppCards.vue';
import { store } from '../store';

export default{
    data() {
    return {
      store
    }
  },

    components: {
    AppCards,
	}
}
</script>

<template>
    <div class="container">
        <!-- TODO: add input component -->
        
        <div class="card-container" >
            <!-- TODO: add counter component -->

        <AppCards v-for="card in store.cardList.data" 
        :key="card.id" 
        :cardsData="card" />
        </div>

    </div>

</template>

<style scoped>
    .container{
        background-color:rgb(212, 143, 56) ;
        height: calc(100Vh - 200px);
    }
</style>