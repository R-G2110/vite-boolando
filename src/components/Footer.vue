<script>

import {menuPrivacy, menuSocial} from '../data/footerMenu';

export default {

	name: 'Footer',
	data() {
		return {
			menuSocial,
			menuPrivacy
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
						<li 
							v-for="(privacy,index) in menuPrivacy"
							:key="index"
						>
							<a :href="privacy.href">{{privacy.text}}</a>
						</li>
					</ul>
				</nav>
			</div>

			<div class="social">
				<h5>Trovaci anche su:</h5>
				<nav>
					<ul class="menu flex">
						<li 
							v-for="(social,index) in menuSocial"
							:key="index"
						>
							<a :href="social.href"><i :class="social.text"></i></a>
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