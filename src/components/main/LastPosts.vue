<template>
	<section id="latest-post" class="container">
		<div id="title" class="text-center">
			<h2>Latest Posts</h2>
			<p>If you are planning on developing a product landing.</p>
		</div>
		<div class="row">
			<div class="col">
				<span>{{ dataCorrente }}</span>
				<img src="../../assets/images/19.jpg" alt="" />
				<h3>Life Lack Meaning</h3>
				<p>
					It is a long established fact that a reader will be
					distracted by the readable.
				</p>
			</div>
			<div class="col">
				<span>{{ dataCorrente }}</span>
				<img src="../../assets/images/18.jpg" alt="" />
				<h3>Life Lack Meaning</h3>
				<p>
					It is a long established fact that a reader will be
					distracted by the readable.
				</p>
			</div>
			<div class="col">
				<span>{{ dataCorrente }}</span>
				<img src="../../assets/images/17.jpg" alt="" />
				<h3>Life Lack Meaning</h3>
				<p>
					It is a long established fact that a reader will be
					distracted by the readable.
				</p>
			</div>
		</div>
	</section>
</template>

<script>
import dayjs from "dayjs";
export default {
	name: "LastPosts",
	data() {
		return {
			dataCorrente: undefined
		};
	},
	created() {
		let giornoCorrente = dayjs().format("MMMM DD, YYYY");
		this.dataCorrente = giornoCorrente;
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
#latest-post {
	margin-bottom: $sectionMargin;
	.col {
		position: relative;
		margin: 0 20px;
		padding: 15px;
		border: 1px solid #0000000d;
		border-radius: 8px;
		span {
			position: absolute;
			margin: 10px;
			padding: 5px 20px;
			border-radius: 5px;
			background: #ffffff;
			color: #8e989f;
			font-weight: 500;
		}
		h3 {
			margin-top: 25px;
			font-size: 20px;
		}
		img {
			width: 100%;
		}
	}
}
</style>
