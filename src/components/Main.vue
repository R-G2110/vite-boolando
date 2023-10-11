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

<style lang="scss" >
@use '../scss/main';

.hide {
	display: none;
}

.container {
	padding-top: 100px;
	flex-wrap: wrap;
	.item {
		margin: 5px auto;
  	width: 350px;
  	display: inline-block;
		overflow: hidden;
		.photo-item {
  		position: relative;
  		cursor: pointer;
			&:hover .alternative{
  			top: 0;
  			left: 0;
  			display: block;
			}
			.alternative{
  			position: absolute;
			}
		}
		.discount {
			font-size: 10px;
			padding: 5px 10px;
			position: absolute;
			bottom: 85px;
			left: 0;
			background-color: red;
			color: white;
		}
		.heart {
  		font-size: 35px;
  		padding: 5px 15px;
  		position: absolute;
  		right: 0;
  		top: 20px;
  		background-color: white;
			&:hover {
  			color: red;
			}
		}
		
		.eco {
 			font-size: 10px;
  		padding: 5px 10px;
  		position: absolute;
  		bottom: 85px;
  		left: 45px;
  		background-color: green;
  		color: white;
		}
		.brand {
  		display: block;
  		font-size: 12px;
		}

		.item-name {
  		display: block;
  		font-size: 14px;
  		font-weight: 700;
  		text-transform: uppercase;
		}

		.c-price {
			color: red;
			font-size: 14px;
			font-weight: 700;
		}

		.o-price {
			margin-left: 10px;
			text-decoration: line-through;
			font-size: 14px;
			font-weight: 700;
			color: rgba($color: #000000, $alpha: 0.4)
		}
		.no-discount .eco{
		  bottom: 85px;
		  left: 0;
		  display: block;
		}
	}
}

</style>