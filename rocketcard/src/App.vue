<template>
  <div id="app">
	  <div>
			<p>Compartilhe seu #rocketcard</p>
			<RocketCard />
	  </div>
		<div>
		  <p>Customizar Rocketcard</p>
			<button @click="toggle">Gerar background</button>
		</div>
	</div>
</template>

<script>
import RocketCard from './components/card.vue'
import { generateColor } from './helpers/color.js'

export default {
  name: 'App',
  components: { RocketCard },
	methods: {
		toggle: () => {
		  const color = generateColor()
			document
			  .querySelector('.wrapper')
				.style
				.backgroundColor = color

			document
			  .querySelector('.avatar')
				.style
				.borderColor = color
		}
	}
}
</script>

<style lang="scss">
@import "./assets/styles/colors.mixin.scss";
@import "./assets/styles/home.mixin.scss";

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	color: $white;

	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

#app {
	@include App;
}
</style>
