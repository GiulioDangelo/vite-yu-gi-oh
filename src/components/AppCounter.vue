<script>
import { store } from '../store';

export default {
    data() {
		return {
			store,
		};
	},
};
</script>

<template>
    <div class="counter">
        Found {{ store.cardList.length }} card
    </div>
</template>

<style scoped>
    .counter{
        background-color: black;
        color: white;
        font-size: 40px;
    }
</style>