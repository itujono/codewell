<template>
	<div id="app">
		<router-view/>
	</div>
</template>

<script>
	export default {
		name: "App"
	}
</script>

<style lang="scss">
	@import "/var.scss";




	@font-face {
		font-family: 'GothamRoundedBold';
		src: url('../src/assets/fonts/gothamrnd-bold.eot');
		src: url('../src/assets/fonts/gothamrnd-bold.eot') format('embedded-opentype'),
			url('../src/assets/fonts/gothamrnd-bold.woff') format('woff'),
			url('../src/assets/fonts/gothamrnd-bold.ttf') format('truetype'),
			url('../src/assets/fonts/gothamrnd-bold.svg#GothamRoundedBold') format('svg');
	}
	
	@font-face {
		font-family: 'GothamRoundedMedium';
		src: url('../src/assets/fonts/gothamrnd-medium.eot');
		src: url('../src/assets/fonts/gothamrnd-medium.eot') format('embedded-opentype'),
			url('../src/assets/fonts/gothamrnd-medium.woff') format('woff'),
			url('../src/assets/fonts/gothamrnd-medium.ttf') format('truetype'),
			url('../src/assets/fonts/gothamrnd-medium.svg#GothamRoundedMedium') format('svg');
	}


	/////////////



	#app {
		font-family: "GothamRoundedBold", Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
	}

	.title {
		color: $yellow;
	}

	.button {
		border-radius: 50px;
		padding-left: 1.75em;
		padding-right: 1.75em;
	}




	@media screen and (max-width: 414px) {
		.container {
			max-width: initial;
		}
	}
</style>
