<script>
	// @ts-nocheck

	import { PrismicLink } from '@prismicio/svelte';
	import { PrismicImage } from '@prismicio/svelte';
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;
</script>

<section class="introduction">
	<section class="introduction-image">
		<PrismicImage field={slice.primary.introduction_image} width="1560px" />
	</section>
	<section class="introduction-title">
		<PrismicRichText field={slice.primary.introduction_title} />
	</section>
	<section class="introduction-bio">
		<PrismicRichText field={slice.primary.introduction_bio} />
	</section>
</section>

<style>
	.introduction {
		position: relative;
		border-radius: 2rem;
	}

	.introduction-title {
		position: absolute;
		top: 2rem;
		width: 20rem;
		margin: 1rem;

		color: #fff;
		font-family: Poppins;
		font-size: 3rem;
		font-style: normal;
		font-weight: 700;
		line-height: 4rem;
	}

	.introduction-bio {
		position: absolute;
		top: 12rem;
		width: 18rem;
		margin: 1rem;

		color: #fff;
		font-family: Poppins;
		font-size: 1.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}

	@media (min-width: 30em) {
		.introduction {
			position: relative;
			border-radius: 2rem;
		}

		.introduction-title {
			position: absolute;
			top: 2rem;
			width: 20rem;
			margin: 2rem;

			color: #fff;
			font-family: Poppins;
			font-size: 3rem;
			font-style: normal;
			font-weight: 700;
			line-height: 4rem;
		}

		.introduction-bio {
			position: absolute;
			top: 12rem;
			width: 18rem;
			margin: 2rem;

			color: #fff;
			font-family: Poppins;
			font-size: 1.5rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}
	}

	@media (min-width: 45em) {
		.introduction {
			position: relative;
			border-radius: 2rem;
		}

		.introduction-title {
			position: absolute;
			top: 1rem;
			width: 36rem;
			margin: 2rem;

			color: #fff;
			font-family: Poppins;
			font-size: 4rem;
			font-style: normal;
			font-weight: 700;
			line-height: 4rem;
		}

		.introduction-bio {
			position: absolute;
			top: 12rem;
			width: 36rem;
			margin: 2rem;

			color: #fff;
			font-family: Poppins;
			font-size: 2rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}
	}
</style>
