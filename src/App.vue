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

  methods: {
    getData() {
      console.log('ciao');
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then(response => (this.store.cardList = response.data))
    },
  },

  created() {
    this.getData()
  },  
}
</script>

<template>
  <AppHeader @filter="this.getData(), event.target.value"/>
  <AppMain/>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  background-color:rgb(212, 143, 56);

}
</style>