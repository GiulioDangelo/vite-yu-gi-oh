<script>
import AppCards from './AppCards.vue';
import AppSelect from './AppSelect.vue';
import AppCounter from '../components/AppCounter.vue'
import { store } from '../store';

export default{
    data() {
    return {
      store
    }
  },

    components: {
    AppCards,
    AppSelect,
    AppCounter
	}
}
</script>

<template>
    <div class="container">
        <AppSelect/>
        <AppCounter/>
        
        <div class="card-container">
        <AppCards v-for="card in store.cardList.data" 
        :key="card.id" 
        :cardsData="card" />
        </div>

    </div>

</template>

<style scoped>
    .container{
        padding: 20px;
        max-width: 1500px;
        margin: auto;
    }

    .card-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        background-color: white;
    }
</style>