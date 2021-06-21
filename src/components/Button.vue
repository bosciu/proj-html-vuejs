<template>
	<button>{{ msg }}</button>
</template>

<script>
export default {
	name: "Button",
	props: {
		msg: {
			type: String,
			required: true
		}
	}
};
</script>

<style lang="scss" scoped>
@import "../styles/variables";
button {
	border-radius: 5px;
	padding: 12px 16px;
	border: unset;
	background-color: $buttonPrimary;
	color: white;
	caret-color: transparent;
	&:focus-visible {
		outline: unset;
	}
}
</style>
