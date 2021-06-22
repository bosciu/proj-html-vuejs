<template>
	<section class="row" id="main-informations">
		<div class="d-flex col-4" v-for="(infoCard, index) in 3" :key="index">
			<div id="img-container">
				<img src="../../assets/images/24.png" alt="PC" />
			</div>
			<div id="informations">
				<h3>Online Marketing</h3>
				<p>
					It is a long established fact that a reader will be
					distracted.
				</p>
				<ul>
					<li><i class="fas fa-check"></i>SEO</li>
					<li><i class="fas fa-check"></i>SEM</li>
					<li><i class="fas fa-check"></i>Website Strategy</li>
					<li><i class="fas fa-check"></i>Social management</li>
				</ul>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "MainInformation"
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
#main-informations {
	margin-bottom: $sectionMargin;
	#img-container {
		img {
			width: 100%;
		}
	}
	#informations {
		padding: 0 25px;
		ul {
			padding-left: 0;
			list-style: none;
			li {
				font-weight: 500;
				margin: 15px 0;
				i {
					display: inline-block;
					margin-right: 12px;
					color: $buttonPrimary;
				}
			}
		}
	}
}
</style>
