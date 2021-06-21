<template>
	<div id="app">
		<Header />
		<Main />
	</div>
</template>

<script>
import Header from "./components/header/Header";
import Main from "./components/main/Main";
export default {
	name: "App",
	components: {
		Header,
		Main
	}
};
</script>

<style lang="scss">
@import "./styles/general";
</style>
