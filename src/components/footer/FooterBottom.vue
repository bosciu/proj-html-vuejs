<template>
	<div id="footer-bottom">
		<div class="container">
			<div class="row">
				<div class="col-3">
					<img src="../../assets/images/35.png" alt="Sofbox logo" />
					<p>
						It is a long established fact that a reader will be
						distracted by the readable content
					</p>
					<span
						>Copyright <em>@</em> 2018
						<span class="color-text">Sofbox</span></span
					>
				</div>
				<div class="col-3">
					<ul>
						<li>Menu</li>
						<li v-for="(link, index) in links[0]" :key="index">
							<a :href="link.url">{{ link.page }}</a>
						</li>
					</ul>
				</div>
				<div class="col-3">
					<ul>
						<li>About Us</li>
						<li v-for="(link, index) in links[1]" :key="index">
							<a :href="link.url">{{ link.page }}</a>
						</li>
					</ul>
				</div>
				<div class="col-3">
					<ul>
						<li>Quick Links</li>
						<li v-for="(link, index) in links[0]" :key="index">
							<a :href="link.url">{{ link.page }}</a>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "FooterBottom",
	props: {
		links: {
			type: Array,
			required: true
		}
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables";
#footer-bottom {
	margin-bottom: $sectionMargin;
	border-top: 2px solid #0000000d;
	.row {
		margin-top: 50px;
		p {
			margin: 10px 0 40px;
		}
		span {
			font-size: 18px;
			color: $lightGreyText;
		}
		.color-text {
			color: $buttonPrimary;
		}
		ul {
			list-style: none;
			& > li:first-child {
				font-size: 20px;
				margin-bottom: 15px;
			}
			& > li:not(li:first-child) {
				margin: 10px 0;
				color: $lightGreyText;
				cursor: pointer;
			}
		}
	}
}
</style>
