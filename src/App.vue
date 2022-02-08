<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
	<header>
		<div>
			<div class="avatar-background">
				<div class="avatar" v-bind:style="{ backgroundImage: 'url(./src/assets/mikel.png)' }"></div>
			</div>
		</div>

		<div class="wrapper">
			<HelloWorld />
		</div>
	</header>

	<main>
		<TheWelcome />
	</main>
</template>

<style lang="scss">
@import "./assets/base.css";

#app {
	//font-family: "Josefin Sans", sans-serif;
	font-family: "Lato", sans-serif;
	max-width: 1280px;
	margin: 0 auto;
	padding: 2rem;

	font-weight: normal;
}

header {
	line-height: 1.5;
}

.avatar-background {
	background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
	background-size: 400% 400%;
	animation: gradient 15s ease infinite;
	border-radius: 50%;
	overflow: hidden;
	width: 125px;
	height: 125px;
	margin: 0 20px 2rem;
	position: relative;
}

.avatar {
	background-size: contain;
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
}

@keyframes gradient {
	0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}

a,
.green {
	text-decoration: none;
	color: hsla(160, 100%, 37%, 1);
	transition: 0.4s;
}

@media (hover: hover) {
	a:hover {
		background-color: hsla(160, 100%, 37%, 0.2);
	}
}

@media (min-width: 1024px) {
	body {
		display: flex;
		place-items: center;
	}

	#app {
		display: grid;
		grid-template-columns: 1fr 1fr;
		padding: 0 2rem;
	}

	header {
		display: flex;
		place-items: center;
		padding-right: calc(var(--section-gap) / 2);
	}

	header .wrapper {
		display: flex;
		place-items: flex-start;
		flex-wrap: wrap;
	}

	.logo {
		margin: 0 2rem 0 0;
	}
}
</style>
