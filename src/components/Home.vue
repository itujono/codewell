<template>
	<section class="hero is-primary is-fullheight">
		<div class="hero-body">
			<div class="container">
				<transition name="slide-fade" mode="out-in" appear>
					<div class="block" v-if="slideThem">
						<h1 class="title">{{msg}}</h1>
						<h3 class="subtitle">Bagaimana mungkin ia bisa memilikinya?</h3>
					</div>
				</transition>
				<div class="block">
					<transition-group name="scaling" tag="ul" mode="out-in" appear>
						<li v-for="icon in icons" :key="icon">
							<b-icon :icon="icon"></b-icon>
						</li>
					</transition-group>
				</div>
				<transition name="scaling" mode="out-in">
					<button class="button is-success" @click="slideThem = !slideThem">Details</button>
				</transition>
			</div>
		</div>
	</section>
</template>

<script>
export default {
  	name: "Home",
  	data() {
		return {
			msg: "Sempardak!",
			slideThem: true,
			iconId: [1, 2, 3, 4, 5, 6, 7],
			icons: ["account", "home", "view-dashboard"]
		}
  	}
}
</script>

<style lang="scss" scoped>
	// .container {
	// 	max-width: 50%;
	// }

	h1, h2 {
		font-weight: normal;
	}

	ul {
		list-style-type: none;
		padding: 0;
		li {
			display: inline-block;
			margin: 0 10px;
		}
	}

	a {
		color: #42b983;
	}

	.slide-fade-enter-active {
		transition: all .4s ease-in-out
	}

	.slide-fade-leave-active, .scaling-leave-active {
		transition: all .1s cubic-bezier(1.0, 0.5, 0.8, 1.0)
	}

	.slide-fade-enter, .slide-fade-leave-to, .scaling-enter {
		opacity: 0;
		transform: translateY(-30px)
	}

	.scaling-enter-active {
		transition: all .6s cubic-bezier(1.0, 0.5, 0.8, 1.0)
	}
</style>
