<script>
export default {
	name: 'Main',
	data() {
		return{

		}
	}
}
</script>

<template>
	<main>

		<div class="container flex justify-center">
		
			<div class="item flex  all-badges">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/1.webp" alt="1">
					<img class="alternative" src="../assets/img/1b.webp" alt="1b">
					<span class="heart">&hearts;</span>
					<span class="discount">50%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Levi's</span>
					<span class="item-name">relaxed fit tee unisex</span>
					<span class="c-price">14,99&euro;</span>
					<span class="o-price">29,99 &euro;</span>
				
				</div>

			</div>
		
			<div class="item flex  no-eco">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/2.webp" alt="1">
					<img class="alternative" src="../assets/img/2b.webp" alt="2b">
					<span class="heart">&hearts;</span>
					<span class="discount">30%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Guess</span>
					<span class="item-name">roses tee</span>
					<span class="c-price">20,99&euro;</span>
					<span class="o-price">29,99 &euro;</span>
				
				</div>

			</div>
		
			<div class="item flex no-eco">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/3.webp" alt="3">
					<img class="alternative" src="../assets/img/3b.webp" alt="3b">
					<span class="heart">&hearts;</span>
					<span class="discount">30%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Come Zucchero Filato</span>
					<span class="item-name">voglia di colori pastello</span>
					<span class="c-price">129,99&euro;</span>
					<span class="o-price">184,99 &euro;</span>
				
				</div>

			</div>
		
			<div class="item flex  all-badges">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/4.webp" alt="4">
					<img class="alternative" src="../assets/img/4b.webp" alt="4b">
					<span class="heart">&hearts;</span>
					<span class="discount">50%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Levi's</span>
					<span class="item-name">tee unisex</span>
					<span class="c-price">14,99&euro;</span>
					<span class="o-price">29,99 &euro;</span>
				
				</div>

			</div>

			<div class="item flex  ">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/5.webp" alt="5">
					<img class="alternative" src="../assets/img/5b.webp" alt="5b">
					<span class="heart">&hearts;</span>
					<span class="discount">50%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Maya Deluxe</span>
					<span class="item-name">stripe bicodice</span>
					<span class="c-price">99,99&euro;</span>
					<span class="o-price">29,99 &euro;</span>
				
				</div>

			</div>

			<div class="item flex  no-discount">
			
				<div class="photo-item">
				
					<img class=" " src="../assets/img/6.webp" alt="6">
					<img class="alternative" src="../assets/img/6b.webp" alt="6b">
					<span class="heart">&hearts;</span>
					<span class="discount">50%</span>
					<span class="eco">Sostenibilità</span>
					<span class="brand ">Esprit</span>
					<span class="item-name">maglione - black</span>
					<span class="c-price">29,99&euro;</span>
					<span class="o-price">29,99 &euro;</span>
				
				</div>

			</div>

		</div>

	</main>
</template>

<style lang="scss" scoped>
@use '../scss/main';

.container {
	padding-top: 100px;
	flex-wrap: wrap;
	.item {
		margin: 5px auto;
  	width: 350px;
  	display: inline-block;
		.photo-item {
  		position: relative;
  		cursor: pointer;
			&:hover .alternative{
  			top: 0;
  			left: 0;
  			display: inline;
			}
			.alternative{
  			position: absolute;
  			display: none;
			}
			.discount {
				z-index: 998;
  			font-size: 10px;
  			padding: 5px 10px;
  			position: absolute;
  			bottom: 85px;
  			left: 0;
  			background-color: red;
  			color: white;
  			display: none;
			}
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
  		display: none;
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
			text-decoration: line-through;
			font-size: 14px;
			font-weight: 700;
			display: none;
		}
		
		
	}
}

</style>