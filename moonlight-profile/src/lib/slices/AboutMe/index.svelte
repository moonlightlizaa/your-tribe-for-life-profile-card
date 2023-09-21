<script>
	// @ts-nocheck

	import { PrismicLink } from '@prismicio/svelte';
	import { PrismicImage } from '@prismicio/svelte';
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;
</script>

<section class="about-me">
	<section class="about-me-title">
		<PrismicRichText field={slice.primary.about_me_title} />
	</section>
	<section class="about-me-intro">
		<PrismicRichText field={slice.primary.about_me_intro} />
	</section>
	<section class="about-me-likes">
		<PrismicRichText field={slice.primary.about_me_likes} />
	</section>
	<section class="about-me-dislikes">
		<PrismicRichText field={slice.primary.about_me_dislikes} />
	</section>
</section>

<style>
	.about-me {
		background-color: #f3f3f3;
		border-radius: 2rem;
		padding: 2rem;
	}
	.about-me-title {
		color: #272727;
		font-family: Poppins;
		font-size: 2.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}

	.about-me-intro {
		padding-bottom: 1rem;

		color: #272727;
		font-family: Poppins;
		font-size: 1.2rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}

	.about-me-likes {
		padding-top: 1rem;
		padding-bottom: 1rem;

		border-top: 1px solid black;

		color: #272727;
		font-family: Poppins;
		font-size: 1.2rem;
		font-weight: 600;
	}

	.about-me-dislikes {
		border-top: 1px solid black;
		padding-top: 1rem;

		color: #272727;
		font-family: Poppins;
		font-size: 1.2rem;
		font-weight: 600;
	}

	@media (min-width: 30em) {
	}

	@media (min-width: 45em) {
		.about-me-title {
			color: #272727;
			font-family: Poppins;
			font-size: 3rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}

		.about-me-intro {
			padding-bottom: 1rem;

			color: #272727;
			font-family: Poppins;
			font-size: 1.5rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}

		.about-me-likes {
			padding-top: 1rem;
			padding-bottom: 1rem;

			border-top: 1px solid black;

			color: #272727;
			font-family: Poppins;
			font-size: 1.375rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}

		.about-me-dislikes {
			border-top: 1px solid black;
			padding-top: 1rem;

			color: #272727;
			font-family: Poppins;
			font-size: 1.375rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}
	}

	@media (min-width: 68em) {
	}
</style>
