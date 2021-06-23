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
						link: "#"
					},
					{
						page: "Theme",
						link: "#"
					},
					{
						page: "Features",
						link: "#"
					},
					{
						page: "Pricing",
						link: "#"
					},
					{
						page: "Blog",
						link: "#"
					}
				],
				[
					{
						page: "About Sofbox",
						link: "#"
					},
					{
						page: "Roadmap",
						link: "#"
					},
					{
						page: "How it Work",
						link: "#"
					},
					{
						page: "Team",
						link: "#"
					},
					{
						page: "News",
						link: "#"
					}
				]
			]
		};
	}
};
</script>

<style></style>
