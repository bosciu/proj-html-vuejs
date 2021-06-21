<template>
	<div id="jumbotron" class="d-flex">
		<div id="text-container">
			<h1>The biggest platform for you growth.</h1>
			<p>
				There are many variations of passages of Lorem Ipsum available,
				but the majority have suffered alteration in some form
			</p>
			<Button msg="Read more" />
		</div>
		<div id="img-container">
			<img src="../../assets/images/27-1.png" alt="Jumbotron" />
		</div>
	</div>
</template>

<script>
import Button from "../Button";
export default {
	name: "Jumbotron",
	components: {
		Button
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
#jumbotron {
	width: 80%;
	height: 500px;
	margin: auto;
	margin-bottom: 10%;
	border-radius: 8px;
	background: $ligthBlueBackground;
	#text-container {
		width: 50%;
		padding: 50px;
		p {
			margin: 2rem 0 3rem;
		}
	}
	#img-container {
		img {
			position: relative;
			top: 40px;
			height: 100%;
		}
	}
}
</style>
