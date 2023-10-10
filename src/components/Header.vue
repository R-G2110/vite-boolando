<script>

import {generePersona, userMenu} from  '../data/headerMenu';

export default {
	name: 'Header',
	data() {
		return{
			generePersona,
			userMenu
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
						<li 
							v-for="(persona, index) in generePersona"
							:key="index"
						>
							<a :href="persona.href">{{persona.text}}</a>
						</li>
					</ul>
				</nav>

				<div class="logo">
					<a href="#">
						<img src="../assets/img/boolean-logo.png" alt="boolean-logo">
					</a>
				</div>
			
				<nav>
					<ul class="flex">
						<li
							v-for="(user, index) in userMenu"
							:key="index"
						>
							<a :href="user.href"><i :class="user.text"></i></a>
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