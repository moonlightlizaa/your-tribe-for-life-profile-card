<script>
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;

	//* this adds images * //
	import { PrismicImage } from '@prismicio/svelte';
</script>

<section class="container">
	<section class="text">
		<PrismicRichText field={slice.primary.bio_text} />
		<PrismicRichText
			field={slice.primary.content}
			components={{
				label: Label
			}}
		/>
	</section>
	<section class="profile-picture">
		<PrismicImage field={slice.primary.profile_picture} />
	</section>
</section>

<style>
	.container {
		max-width: 1400px;
		margin: 4em auto;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif,
			'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';
		display: grid;
		grid:
			'profile-picture text' 1fr
			/ 1fr 1fr;
		gap: 20px;
	}

	.profile-picture {
		grid-area: profile-picture;
	}
	.text {
		grid-area: text;
	}
</style>
