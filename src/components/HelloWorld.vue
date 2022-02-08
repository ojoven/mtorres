<script setup>
defineProps({
	msg: {
		type: String,
		required: false
	}
})
</script>

<template>
	<div class="greetings">
		<h1 class="green">Hi, my name is Mikel</h1>
		<h3>And I'm a senior web developer & technical lead that focuses on creating great products for clients and users.</h3>
	</div>
</template>

<style scoped>
h1 {
	font-family: "Josefin Sans", sans-serif;
	font-weight: 700;
	font-size: 2.6rem;
	top: -10px;
	line-height: 1;
	color: #3b368c;
}

h3 {
	font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
	text-align: center;
}

@media (min-width: 1024px) {
	.greetings h1,
	.greetings h3 {
		text-align: left;
	}
}
</style>
