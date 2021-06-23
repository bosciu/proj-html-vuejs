<template>
	<form @submit.prevent>
		<div class="mb-4 name-email">
			<input type="text" class="form-control" placeholder="Your Name" />
			<input type="email" class="form-control" placeholder="Your Email" />
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
</template>

<script>
import Button from "../Button";
export default {
	name: "Form",
	components: {
		Button
	}
};
</script>

<style lang="scss" scoped>
form {
	input,
	textarea {
		padding: 10px 15px;
		caret-color: black;
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
</style>
