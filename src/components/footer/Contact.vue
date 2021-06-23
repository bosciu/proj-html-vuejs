<template>
	<section id="contact" class="container">
		<div id="title" class="text-center">
			<h2>Contact with our team</h2>
			<p>If you are planning on developing a product landing</p>
		</div>
		<div class="row">
			<div class="col-6 maps">
				<iframe
					width="555"
					height="450"
					style="border: 0"
					loading="lazy"
					allowfullscreen
					src="https://www.google.com/maps/embed/v1/place?q=place_id:EihTdG9yZXkgQXZlLCBTYW4gRnJhbmNpc2NvLCBDQSA5NDEyOSwgVVNBIi4qLAoUChIJoRUmMOaGhYARAHx1UQITvYYSFAoSCSEAaQBtmoWAEf-tdvBnE1BK&key=AIzaSyDGFDrCh1MOK-wxSZpwvR0Auw3MHevHgw0"
				></iframe>
			</div>
			<div class="col-6">
				<img src="../../assets/images/35.png" alt="Sofbox logo" />
				<h3>9840 Shore St. Found Du Lac, WI 54935</h3>
				<span>0 1223 456 789</span>
				<span>mail@sofbox.com</span>
				<div class="socials">
					<i class="fab fa-facebook-f"></i>
					<i class="fab fa-twitter"></i>
					<i class="fab fa-github"></i>
					<i class="fab fa-instagram"></i>
				</div>
				<h3>Get in Touch</h3>
				<form @submit.prevent>
					<div class="mb-4 name-email">
						<input
							type="text"
							class="form-control"
							placeholder="Your Name"
						/>
						<input
							type="email"
							class="form-control"
							placeholder="Your Email"
						/>
					</div>
					<div class="mb-4 subject">
						<input
							type="text"
							class="form-control"
							placeholder="Your Subject"
						/>
					</div>
					<div class="mb-4 text-area">
						<textarea
							class="form-control"
							aria-label="With textarea"
							placeholder="Your Message"
						></textarea>
					</div>
					<Button msg="Send Message" />
				</form>
			</div>
		</div>
	</section>
</template>

<script>
import Button from "../Button";
export default {
	name: "Contact",
	components: {
		Button
	}
};
</script>

<style lang="scss" scoped>
@import "../../styles/variables";
#contact {
	margin-bottom: $sectionMargin;
	p {
		margin-top: 30px;
		margin-bottom: 100px;
	}
	.maps {
		text-align: center;
	}

	h3 {
		margin: 30px 0 40px;
		font-size: 20px;
	}
	span {
		display: block;
		margin: 10px 0;
		color: $lightGreyText;
	}
	.socials {
		margin-top: 50px;
		i {
			display: inline-block;
			width: 40px;
			height: 40px;
			margin-right: 10px;
			border: 1px solid #0000000d;
			border-radius: 8px;
			line-height: 40px;
			text-align: center;
			color: $buttonPrimary;
			cursor: pointer;
		}
	}
	form {
		input,
		textarea {
			padding: 10px 15px;
		}
		.name-email {
			display: flex;
			justify-content: space-between;
			.form-control {
				width: 45%;
			}
		}
		textarea {
			min-height: 200px;
		}
	}
}
</style>
