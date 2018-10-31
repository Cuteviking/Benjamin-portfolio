<template>
  <header class="header">
  	<div :class="['link-wrapper', 'left', {active: !isNotFrontpage()}]">
  		<nuxt-link to="work">My work</nuxt-link>
  	</div>
  	<div class="logo-wrapper">
  		<nuxt-link to="/">
  			<img src="~/static/b.svg">
  		</nuxt-link>
  	</div>
  	<div :class="['link-wrapper', 'right', {active: !isNotFrontpage()}]">
  		<nuxt-link to="contact">Contact me</nuxt-link>
  	</div>
  </header>
</template>
<script>
export default {
	methods: {
		isNotFrontpage() {
			if(this.$route.path == '/') {
				return true
			} else {
				return false
			}
		}
	}
}
</script>
<style lang="scss">
	.header {
		z-index: 100;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		text-align: center;

		>* {
			display: inline-block;
			line-height: 70px; 
			height: 70px;
		}

		.link-wrapper {
			
			margin: 0 20px;
			position: relative;

			transition: 0.4s;
			opacity: 0;
			transform: translateY(-20px);

			&.active {
				transform: translateY(0);
				opacity: 1;
			}
		}

		.logo-wrapper {
			width: 70px;

			img {
				width: 100%;
				margin-top: -4px;
			}

			a:after {
				display: none;
			}
		}
	}
</style>
