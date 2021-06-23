<template>
	<div id="navbar" class="d-flex align-items-center">
		<nav>
			<ul>
				<li v-for="(link, index) in links" :key="link.name">
					<a
						:href="link.url"
						:class="link.active ? 'active' : ''"
						@click="$emit('changeActive', index)"
						>{{ link.name }}</a
					>
				</li>
			</ul>
		</nav>
		<div id="shop-icons">
			<a href="#"><i class="fas fa-search"></i></a>
			<a href="#"><i class="fas fa-shopping-cart"></i></a>
		</div>
		<Button msg="Get Started" />
	</div>
</template>

<script>
import Button from "../Button";
export default {
	name: "Navbar",
	components: {
		Button
	},
	props: {
		links: {
			type: Array,
			required: true
		}
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
#navbar {
	margin-left: auto;
	nav {
		& > ul {
			margin-bottom: 0;
			list-style: none;
			& > li {
				display: inline-block;
				margin: 0 15px;
				font-size: 17px;
				font-weight: 500;
				cursor: pointer;
				.active::after {
					content: "";
					display: block;
					position: relative;
					top: 15px;
					width: 100%;
					height: 2px;
					background-color: $buttonPrimary;
				}
			}
		}
	}
	#shop-icons {
		margin: 0 30px;
		font-size: 18px;
		a {
			display: inline-block;
			margin: 0 10px;
			color: black;
		}
	}
}
</style>
