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
	<section class="introduction-title">
		<PrismicRichText field={slice.primary.introduction_title} />
	</section>
	<section class="introduction-bio">
		<PrismicRichText field={slice.primary.introduction_bio} />
	</section>
	<section class="introduction-image">
		<PrismicImage field={slice.primary.introduction_image} />
	</section>
</section>

<style>
	.introduction-title {
		font-family: Poppins;
		font-size: 6rem;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
	}

	.introduction-bio {
		font-family: Poppins;
		font-size: 2rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}
</style>
