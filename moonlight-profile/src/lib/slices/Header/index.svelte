<script>
	import { PrismicLink } from '@prismicio/svelte';
	import { PrismicImage } from '@prismicio/svelte';
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;
</script>

<section class="header">
	<section class="header-profile-image">
		<PrismicImage field={slice.primary.header_profile_image} width="65px" />
	</section>
	<section class="header-profile-name">
		<PrismicRichText field={slice.primary.header_profile_name} />
	</section>
	<section class="header-profile-button">
		<PrismicLink field={slice.primary.header_social_button}>GitHub</PrismicLink>
	</section>
</section>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Syncopate:wght@700&display=swap');

	.header {
		background-color: #f3f3f3;
		display: grid;
		grid:
			'picture name' 1fr
			/ 1fr 2fr;
		gap: 10px;

		border-radius: 2rem;
		padding: 0rem;
	}

	.header-profile-image {
		grid-area: picture;
		padding-left: 2rem;
	}

	.header-profile-name {
		grid-area: name;
		color: #272727;
		font-family: Poppins;
		font-size: 1.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;

		padding-top: 1rem;
	}

	.header-profile-button {
		display: none;
	}

	@media (min-width: 31em) {
	}

	@media (min-width: 45em) {
		.header {
			display: grid;
			grid:
				'picture name social' 1fr
				/ 0.5fr 1fr 1fr;
			gap: 10px;
		}

		.header-profile-button {
			display: none;
			grid-area: social;

			color: #272727;
			font-family: Poppins;
			font-size: 1.5rem;

			font-weight: 600;
		}
	}

	@media (min-width: 68em) {
	}
</style>
