<script>
	// @ts-nocheck

	/** @type {import("@prismicio/client").Content.ChatSlice} */
	import { PrismicLink } from '@prismicio/svelte';
	import { PrismicImage } from '@prismicio/svelte';
	import { PrismicRichText } from '@prismicio/svelte';
	import Label from './Label.svelte';

	/** @type {import("@prismicio/client").Content.RichTextSlice} */
	export let slice;
</script>

<section class="chat">
	<section class="chat-title">
		<PrismicRichText field={slice.primary.chat_title} />
	</section>
</section>

<style>
	.chat {
		background-color: #f3f3f3;
		border-radius: 20px;
		padding: 2rem;
	}

	.chat-title {
		color: #272727;
		font-family: Poppins;
		font-size: 2.5rem;
		font-style: normal;
		font-weight: 600;
		line-height: normal;
	}

	@media (min-width: 45em) {
		.chat {
			background-color: #f3f3f3;
			border-radius: 20px;
		}

		.chat-title {
			color: #272727;
			font-family: Poppins;
			font-size: 3rem;
			font-style: normal;
			font-weight: 600;
			line-height: normal;
		}
	}
</style>
