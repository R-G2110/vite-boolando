<script>
export default {
	name: 'Footer',
	data() {
		return{

		}
	}
}
</script>

<template>
	<footer>
		<div class="container flex justify-sb">

			<div class="privacy">
			
				<h4>Boolando s.r.l</h4>
				<nav>
				
					<ul class="menu flex">
					
						<li>
							
							<a href="@">Informazioni legali</a>
						
						</li>
					
						<li>
							
							<a href="@">Informativa sulla privacy</a>
						
						</li>
					
						<li>
							
							<a href="@">Diritto di recesso</a>
						
						</li>
					
					</ul>
				
				</nav>
			
			</div>

			<div class="social">

				<h5>Trovaci anche su</h5>
				<nav>

					<ul class="menu flex">

						<li>

							<a href="#">

								<i class="fa-brands fa-square-twitter"></i>

							</a>

						</li>

						<li>

							<a href="#">

								<i class="fa-brands fa-square-facebook"></i>

							</a>

						</li>

						<li>

							<a href="#">

								<i class="fa-brands fa-square-instagram"></i>

							</a>

						</li>

						<li>

							<a href="#">

								<i class="fa-brands fa-square-pinterest"></i>

							</a>

						</li>

						<li>

							<a href="#">

								<i class="fa-brands fa-square-youtube"></i>

							</a>

						</li>

					</ul>

				</nav>

			</div>

		</div>
	</footer>
</template>

<style lang="scss" scoped>
	@use '../scss/main';

	h5,
	h4 {
		color: white;
	}

	a:hover {
		color: #FF6900;
	}

	footer{
	  margin-top: 50px;
	  padding: 20px;
	  background-color: #1A1A1A;
		.privacy a {
		  font-size: 10px;
		}
		.social ul li{
		  list-style: none;
		}
	}
</style>