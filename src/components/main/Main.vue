<template>
	<main class="container">
		<!-- Prima sezione con informazioni principali -->
		<section class="row" id="main-informations">
			<div
				class="d-flex col-4"
				v-for="(infoCard, index) in 3"
				:key="index"
			>
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
		<!-- /Prima sezione con informazioni principali -->
		<!-- Seconda sezione con informazioni secondarie -->
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
		<!-- /Seconda sezione con informazioni secondarie -->
	</main>
</template>

<script>
export default {
	name: "Main"
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
#secondary-informations {
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
		#reporting-analysis {
			box-shadow: 0 25px 30px rgba(0, 0, 0, 10%);
		}
	}
}
</style>
