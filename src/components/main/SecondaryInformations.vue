<template>
	<section class="row" id="secondary-informations">
		<div class="col-6" id="information">
			<h2>Get tips tricks on how to skyrocket your sales.</h2>
			<p>
				Faff about only a quid blower i don't want no aggro bleeding
				chimney pot burke tosser cras nice one boot fanny.!
			</p>
			<div id="reporting-analysis" class="d-flex align-items-center">
				<div class="img-container">
					<img src="../../assets/images/510.png" alt="" />
				</div>
				<div class="text-container">
					<h3>Reporting Analysis</h3>
					<p>
						It is a long established fact that a reader will be
						distracted by the readable content of a page when
						looking at is layout.
					</p>
				</div>
			</div>
			<div id="technical-seo" class="d-flex align-items-center">
				<div class="img-container">
					<img src="../../assets/images/511.png" alt="" />
				</div>
				<div class="text-container">
					<h3>Technical SEO Audit</h3>
					<p>
						It is a long established fact that a reader will be
						distracted by the readable content of a page when
						looking at is layout.
					</p>
				</div>
			</div>
		</div>
		<div class="col-6" id="img-container">
			<img src="../../assets/images/509.jpeg" alt="" />
		</div>
	</section>
</template>

<script>
export default {
	name: "SecondaryInformation"
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
#secondary-informations {
	margin-bottom: $sectionMargin;
	& > #information {
		h3 {
			font-size: 20px;
		}
		& > p {
			margin: 15px 0 50px;
		}
		#reporting-analysis,
		#technical-seo {
			padding: 25px 70px 25px 10px;
			.img-container {
				margin-right: 10px;
			}
			h3 {
				color: $buttonPrimary;
				font-weight: 500;
			}
			p {
				margin-bottom: 0;
				font-weight: 500;
			}
		}
		#technical-seo {
			margin-top: 15px;
			h3 {
				color: black;
			}
		}
		#reporting-analysis {
			box-shadow: 0 25px 30px rgba(0, 0, 0, 10%);
		}
	}
}
</style>
