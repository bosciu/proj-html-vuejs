<template>
	<main>
		<div class="container">
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
							<li>
								<i class="fas fa-check"></i>Website Strategy
							</li>
							<li>
								<i class="fas fa-check"></i>Social management
							</li>
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
						Faff about only a quid blower i don't want no aggro
						bleeding chimney pot burke tosser cras nice one boot
						fanny.!
					</p>
					<div
						id="reporting-analysis"
						class="d-flex align-items-center"
					>
						<div class="img-container">
							<img src="../../assets/images/510.png" alt="" />
						</div>
						<div class="text-container">
							<h3>Reporting Analysis</h3>
							<p>
								It is a long established fact that a reader will
								be distracted by the readable content of a page
								when looking at is layout.
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
								It is a long established fact that a reader will
								be distracted by the readable content of a page
								when looking at is layout.
							</p>
						</div>
					</div>
				</div>
				<div class="col-6" id="img-container">
					<img src="../../assets/images/509.jpeg" alt="" />
				</div>
			</section>
			<!-- /Seconda sezione con informazioni secondarie -->
			<!-- Terza sezione Features -->
		</div>
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
							:src="
								require('../../assets/images' + feature.imgPath)
							"
							alt=""
						/>
					</div>
				</div>
			</div>
		</section>
		<!-- /Terza sezione Features -->
	</main>
</template>

<script>
import Button from "../Button";
export default {
	name: "Main",
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
#features {
	position: relative;
	& > img {
		position: absolute;
		right: 87%;
		bottom: 0;
		z-index: -10;
	}
	&::after {
		content: "";
		display: table;
		clear: both;
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
