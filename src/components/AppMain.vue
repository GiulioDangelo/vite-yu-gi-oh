<script>
import AppCards from './AppCards.vue';
import AppSelect from './AppSelect.vue';
import AppCounter from '../components/AppCounter.vue'
import { store } from '../store';

export default{
    data() {
    return {
      store,
    }
  },

    components: {
    AppCards,
    AppSelect,
    AppCounter
	},
  methods: {
    getData() {
      if (value == this.event.target.value) {
      console.log('ciao');
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
      .then(response => (this.store.cardList = response.data));  
      }
    },
  },
}
</script>

<template>
    <div class="container">
        <AppSelect @filter="this.getData(), event.target.value"/>
        <AppCounter/>
    
        <!-- FIXME: -->
        <div class="card-container">
        <AppCards v-for="card in store.cardList" 
        :key="card.id" 
        :cardsData="card" 
        />
        </div>

        <!-- <div class="loading">Loading...</div> -->
      

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

    .loading{
      font-size: 50px;  
      color: white;
    }
</style>