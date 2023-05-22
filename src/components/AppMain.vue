<script>
import AppCards from './AppCards.vue';
import AppSelect from './AppSelect.vue';
import { store } from '../store';

export default{
    data() {
    return {
      store
    }
  },

    components: {
    AppCards,
    AppSelect
	}
}
</script>

<template>
    <div class="container">
        <AppSelect/>
        
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
        background-color:rgb(212, 143, 56);
        padding: 20px;
    }

    .card-container{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        background-color: white;
    }
</style>