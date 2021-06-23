<template>
	<section id="testimonials">
		<img src="../../assets/images/15.png" alt="background" />
		<div class="container text-center">
			<h2>Our Testimonials</h2>
			<p>
				If you are planning on developing a product landing app or
				website,<br />take a look at this beautiful-crafted
			</p>
			<div class="review">
				<img src="../../assets/images/26.jpeg" alt="Woman" />
				<img
					src="../../assets/images/quotation.png"
					alt=""
					class="background"
				/>
				<h3>Julia Aann <span>- COO Sofbox</span></h3>
				<p>
					At vero eos et accusamus et iusto odio dignissimos ducimus
					qui blanditiis praesentium vero eos et consectetur accus
					adip adip
				</p>
				<div class="second-card"></div>
				<div class="third-card"></div>
			</div>
			<div class="review r-right">
				<img src="../../assets/images/25.jpeg" alt="Man" />
				<img
					src="../../assets/images/quotation.png"
					alt=""
					class="background"
				/>
				<h3>Mac Znder <span>- Manager Sofbox</span></h3>
				<p>
					At vero eos et accusamus et iusto odio dignissimos ducimus
					qui blanditiis praesentium vero eos et consectetur accus
					adip adip
				</p>
				<div class="second-card"></div>
				<div class="third-card"></div>
			</div>
			<div id="review-select">
				<div class="selected active"></div>
				<div class="selected"></div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "Testimonials"
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
@import "../../styles/mixins.scss";
#testimonials {
	position: relative;
	margin-bottom: $sectionMargin;
	overflow-x: clip;
	img[src*="15"] {
		position: absolute;
		left: -4%;
		top: -8%;
		z-index: -20;
		transform: scale(1.5);
		background: linear-gradient(180deg, #deebff, transparent);
	}
	.container {
		@include clearfix;
	}
	p {
		margin: 30px 0 60px;
	}
	& .r-right {
		margin-left: 70px;
	}
	.review {
		float: left;
		position: relative;
		background-color: white;
		width: calc(100% / 2 - 35px);
		padding: 50px;
		& > img:first-child {
			width: 80px;
			height: 80px;
			border: 3px solid white;
			border-radius: 50%;
		}
		img.background {
			width: 15%;
			@include absoluteCenter;
			opacity: 0.1;
		}
		h3 {
			margin: 30px 0;
			font-size: 22px;
			span {
				color: $lightGreyText;
			}
		}
		p {
			text-align: left;
		}
		.second-card {
			position: absolute;
			top: 54%;
			z-index: -1;
			width: 85%;
			height: 200px;
		}
		.third-card {
			position: absolute;
			top: 58%;
			right: 13%;
			z-index: -2;
			width: 70%;
			height: 200px;
		}
		&,
		.second-card,
		.third-card {
			border-radius: 5px;
			background-color: white;
			box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
		}
	}
	#review-select {
		.selected {
			display: inline-block;
			width: 12px;
			height: 12px;
			margin: 60px 5px;
			border-radius: 5px;
			background-color: black;
			cursor: pointer;
			&.active {
				background-color: $buttonPrimary;
			}
		}
	}
}
</style>
