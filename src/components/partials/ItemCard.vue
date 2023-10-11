<script>

export default {
	name:'ItemCard',
	props: {
		itemObj: Object
	},
	data(){
		return{

		}
	},
	computed: {

	}
}
</script>

<template>
	<div class="item flex all-badges">
	
		<div class="photo-item">
		
			<img 
				:src="`/img/${itemObj.photo}`" 
				:alt="itemObj.photo"
			>
			<img 
				class="alternative" 
				:src="`/img/${itemObj.alternative}`" 
				:alt="itemObj.alternative"
			>
			<span class="heart">&hearts;</span>
			<span 
				:class="{'hide': itemObj.discount === '0%'}"
				class="discount"
			>{{itemObj.discount}}</span>
			<span 
				:class="{'hide': itemObj.eco === false}"
				class="eco"
			>Sostenibilità</span>
			<span class="brand">{{itemObj.brand}}</span>
			<span class="item-name">{{itemObj.itemName}}</span>
			<span class="c-price">{{itemObj.currPrice}}&euro;</span>
			<span 
				:class="{'hide': itemObj.discount === '0%'}"
				class="o-price"
			>{{itemObj.origPrice}}&euro;</span>
		
		</div>
	</div>
</template>

<style lang="scss" scoped>
.hide {
	display: none;
}

.container {
	padding-top: 100px;
	flex-wrap: wrap;
	.item {
		margin: 5px auto;
  	width: 390px;
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