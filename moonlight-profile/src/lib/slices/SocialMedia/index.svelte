<script>
	// @ts-nocheck

	import { PrismicLink } from '@prismicio/svelte';
	import { PrismicImage } from '@prismicio/svelte';
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;
</script>

<section class="social-media">
	<section class="social-media-title">
		<PrismicRichText field={slice.primary.social_media_title} />
	</section>
	<section class="social-media-option-1">
		<PrismicLink field={slice.primary.social_media_option1}>LinkedIn</PrismicLink>
	</section>
	<section class="social-media-option-2">
		<PrismicLink field={slice.primary.social_media_option2}>Spotify</PrismicLink>
	</section>
	<section class="social-media-option-3">
		<PrismicLink field={slice.primary.social_media_option3}>GitHub</PrismicLink>
	</section>
</section>

<style>
	.social-media {
		display: grid;
		grid:
			'title' 1fr
			'option1' 1fr
			'option2' 1fr
			'option3' 1fr
			/ 1fr;
		gap: 20px;

		background-color: #f3f3f3;
		border-radius: 2rem;
		padding: 2rem;
	}

	.social-media-title {
		grid-area: title;

		color: #272727;
		font-family: Poppins;
		font-size: 3rem;
		font-style: normal;
		font-weight: 600;
		line-height: 107%; /* 3.21rem */
		letter-spacing: 0.045rem;
	}

	.social-media-option-1 {
		grid-area: option1;

		color: #272727;
		font-family: Poppins;
		font-size: 1.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}
	.social-media-option-2 {
		grid-area: option2;

		color: #272727;
		font-family: Poppins;
		font-size: 1.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}
	.social-media-option-3 {
		grid-area: option3;

		color: #272727;
		font-family: Poppins;
		font-size: 1.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}
</style>
