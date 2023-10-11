<script>

import items from '../data/mainData';
import ItemCard from './partials/itemCard.vue';

export default {
	name: 'Main',
	components:{
		ItemCard
	},
	data() {
		return{
			items
		}
	},
	methods: {
		getImagePath(img){
			return new URL(`../assets/img/${img}`,import.meta.url).href;
		}
	},
}
</script>

<template>
	<main>

		<div class="container flex justify-center">
			<ItemCard 
				v-for="(item,index) in items"
				:key="index"
				:itemObj="item"
			/>
		</div>
		
	</main>
</template>

<style lang="scss" scoped>
@use '../scss/main';
.container {
	padding-top: 100px;
	flex-wrap: wrap;
}


</style>