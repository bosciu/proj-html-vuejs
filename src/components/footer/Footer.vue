<template>
	<footer>
		<Contact />
		<FooterBottom :links="footerLinks" />
	</footer>
</template>

<script>
import Contact from "./Contact";
import FooterBottom from "./FooterBottom";
export default {
	name: "Footer",
	components: {
		Contact,
		FooterBottom
	},
	data() {
		return {
			footerLinks: [
				[
					{
						page: "About Us",
						url: "#"
					},
					{
						page: "Theme",
						url: "#"
					},
					{
						page: "Features",
						url: "#"
					},
					{
						page: "Pricing",
						url: "#"
					},
					{
						page: "Blog",
						url: "#"
					}
				],
				[
					{
						page: "About Sofbox",
						url: "#"
					},
					{
						page: "Roadmap",
						url: "#"
					},
					{
						page: "How it Work",
						url: "#"
					},
					{
						page: "Team",
						url: "#"
					},
					{
						page: "News",
						url: "#"
					}
				]
			]
		};
	}
};
</script>

<style></style>
