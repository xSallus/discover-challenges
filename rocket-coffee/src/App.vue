<script setup lang="ts">
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Toast from './components/Toast.vue'
</script>

<template>
  <Header />
  <Main />
	<Toast />
</template>

<style lang="scss">
@import "./colors.scss";

* {
  margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: 'Manrope', sans-serif;
	color: $text;
}

#app {
  height: 100vh;
	width: 100vw;
	background-color: $bg;
	background-image: url(assets/rocket-coffee.png);
	background-position: bottom;
	background-repeat: no-repeat;
	background-size: 90%;
}

a {
	text-decoration: none;
}

button {
	&:active {
		filter: brightness(0.68);
	}

	@media(min-width: 1024px) {
		&:hover {
			filter: brightness(0.68);
		}
	}
}
</style>
