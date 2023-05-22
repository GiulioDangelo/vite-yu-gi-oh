<script>
import { store } from './store'
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import axios from 'axios';

export default {
  data() {
    return {
      store
    }
  },
  
  components: {
		AppHeader,
		AppMain,
	},
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=30&offset=0')
    .then(response => (this.store.cardList = response.data))
  },  
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color:rgb(212, 143, 56);
}
</style>