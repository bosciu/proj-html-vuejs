<template>
	<header>
		<div id="header-top" class="container d-flex align-items-center">
			<div id="logo-container" class="h-100">
				<img src="../../assets/images/logo-2.png" alt="Sofbox" />
			</div>
			<Navbar :links="headerLinks" @changeActive="changeActive" />
		</div>
		<Jumbotron />
	</header>
</template>

<script>
import Navbar from "./Navbar";
import Jumbotron from "./Jumbotron";
export default {
	name: "Header",
	components: {
		Navbar,
		Jumbotron
	},
	data() {
		return {
			headerLinks: [
				{ name: "Home", url: "#", active: true },
				{ name: "About us", url: "#", active: false },
				{ name: "Feature", url: "#", active: false },
				{ name: "Testimonials", url: "#", active: false },
				{ name: "Contact us", url: "#", active: false }
			]
		};
	},
	methods: {
		changeActive(index) {
			this.headerLinks.forEach((link) => {
				link.active = false;
			});
			this.headerLinks[index].active = true;
		}
	}
};
</script>

<style lang="scss" scoped>
#header-top {
	height: 75px;
	padding: 15px 50px;
	margin-bottom: 20px;
	a {
		color: unset;
		text-decoration: none;
	}
	#logo-container {
		img {
			height: 100%;
			transform: scale(1.3);
		}
	}
}
</style>
