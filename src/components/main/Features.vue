<template>
	<section id="features">
		<img
			src="../../assets/images/14.png"
			alt="background"
			class="features-background"
		/>
		<div class="container pe-5">
			<div
				class="
					heading
					d-flex
					align-items-center
					justify-content-between
				"
			>
				<div class="title">
					<h2>Popular features that your business needs</h2>
					<p>
						Faff about only a quid blower i don't want no agro
						bleeding chimney pot burke tosser cras nice one boot
						fanny.!
					</p>
				</div>
				<Button msg="Explore more features" />
			</div>
			<div class="features-container">
				<div
					class="card"
					v-for="(feature, index) in features"
					:key="index"
				>
					<h4>
						{{ feature.id }}
					</h4>
					<img
						:src="require('../../assets/images' + feature.imgPath)"
						alt=""
					/>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import Button from "../Button";
export default {
	name: "Features",
	components: {
		Button
	},
	data() {
		return {
			features: [
				{
					id: "Customized Invoices",
					imgPath: "/financial-presentation.png",
					link: "#"
				},
				{
					id: "Stock Management",
					imgPath: "/paper-plane.png",
					link: "#"
				},
				{
					id: "Receivable & Paybles",
					imgPath: "/bill.png",
					link: "#"
				},
				{
					id: "Manage Buying",
					imgPath: "/financial-presentation.png",
					link: "#"
				},
				{
					id: "Powerful & Secure",
					imgPath: "/paper-plane.png",
					link: "#"
				},
				{
					id: "Fastest Return Filing",
					imgPath: "/bill.png",
					link: "#"
				},
				{
					id: "Monthly Detailed",
					imgPath: "/financial-presentation.png",
					link: "#"
				},
				{
					id: "Product Management",
					imgPath: "/paper-plane.png",
					link: "#"
				}
			]
		};
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
@import "../../styles/mixins.scss";
#features {
	position: relative;
	margin-bottom: $sectionMargin;
	& > img {
		position: absolute;
		right: 87%;
		bottom: 0;
		z-index: -10;
	}
	&::after {
		@include clearfix;
	}
	.title {
		p {
			width: 65%;
		}
	}
	.card {
		width: calc(100% / 4 - 30px);
		margin: 15px;
		padding: 25px 20px 40px;
		border: none;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 10%);
		float: left;
		img {
			width: 20%;
		}
	}
}
</style>
