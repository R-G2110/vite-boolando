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
				:class="{'hide': itemObj.discount === '0'}"
				class="discount"
			>{{itemObj.discount}}%</span>
			<span 
				:class="{'hide': itemObj.eco === false}"
				class="eco"
			>Sostenibilità</span>
			<span class="brand">{{itemObj.brand}}</span>
			<span class="item-name">{{itemObj.itemName}}</span>
			<span class="c-price">{{itemObj.currPrice}}&euro;</span>
			<span 
				:class="{'hide': itemObj.discount === '0'}"
				class="o-price"
			>{{itemObj.origPrice}}&euro;</span>
		
		</div>
	</div>
</template>

<style lang="scss">

</style>