<script>
export default {
	name: 'Header',
	data() {
		return{

		}
	}
}
</script>

<template>
	<header>

		<div class="fixed  ">
		
			<div class="container flex justify-sb">
			
				<nav>
				
					<ul class="flex">
					
						<li>
							<a href="#">Donna</a>
						</li>
					
						<li>
							<a href="#">Uomo</a>
						</li>
					
						<li>
							<a href="#">Bambini</a>
						</li>
					
					</ul>
				
				</nav>

				<div class="logo">

					<a href="">
						<img src="../assets/img/boolean-logo.png" alt="boolean-logo">
					</a>
				
				</div>
			
				<nav>
				
					<ul class="flex">
					
						<li>
						
							<a href="#">
								<i class="fa-solid fa-user-astronaut"></i>
							</a>
						
						</li>
					
						<li>
						
							<a href="#">
								<i class="fa-regular fa-heart"></i>
							</a>
						
						</li>
					
						<li>
						
							<a href="#">
								<i class="fa-solid fa-bag-shopping"></i>
							</a>
						
						</li>
					
					</ul>
				
				</nav>
			
			</div>
		
		</div>

</header>
</template>

<style lang="scss" scoped>

@use '../scss/partials/utilities' as *;
@use '../scss/partials/general' as *;


header .fixed{
	width: 100%;
  height: 70px;
  background-color: #FF6900;
	position: fixed;
	z-index: 999;
	.container {
		align-items: center;
		.logo {
			width: 150px;
		}
	}
}

</style>