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
