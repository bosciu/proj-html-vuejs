<template>
	<main>
		<div class="container">
			<!-- Prima sezione con informazioni principali -->
			<MainInformation />
			<!-- Seconda sezione con informazioni secondarie -->
			<SecondaryInformation />
		</div>
		<!-- Sezione con features del sito -->
		<Features />
		<!-- Sezione testimonials con frase -->
		<Testimonials />
		<!-- Ultimi articoli pubblicati -->
		<LastPosts />
	</main>
</template>

<script>
import MainInformation from "./MainInformation";
import SecondaryInformation from "./SecondaryInformations";
import Features from "./Features";
import Testimonials from "./Testimonials";
import LastPosts from "./LastPosts";
export default {
	name: "Main",
	components: {
		MainInformation,
		SecondaryInformation,
		Features,
		Testimonials,
		LastPosts
	}
};
</script>

<style></style>
