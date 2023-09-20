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
		<PrismicLink field={slice.primary.header_social_button}
			>GitHub <svg
				width="50"
				height="50"
				viewBox="0 0 52 52"
				fill="none"
				xmlns="http://www.w3.org/2000/svg"
				class="header-arrow"
			>
				<path
					d="M43.3335 26L43.687 25.6464L44.0406 26L43.687 26.3536L43.3335 26ZM10.8335 26.5C10.5574 26.5 10.3335 26.2761 10.3335 26C10.3335 25.7239 10.5574 25.5 10.8335 25.5V26.5ZM30.687 12.6464L43.687 25.6464L42.9799 26.3536L29.9799 13.3536L30.687 12.6464ZM43.687 26.3536L30.687 39.3536L29.9799 38.6464L42.9799 25.6464L43.687 26.3536ZM43.3335 26.5H10.8335V25.5H43.3335V26.5Z"
					fill="#272727"
				/>
			</svg></PrismicLink
		>
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
				/ 0.5fr 1fr 2fr;
			gap: 10px;
		}

		.header-profile-button {
			display: block;
			grid-area: social;

			color: #272727;
			font-family: Poppins;
			font-size: 1.5rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}
	}

	@media (min-width: 68em) {
	}
</style>
