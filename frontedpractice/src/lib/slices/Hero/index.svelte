<script>
	import { PrismicImage, PrismicRichText, PrismicLink } from '@prismicio/svelte';
	import { isFilled } from '@prismicio/client';

	/**
	 * @type {import("@prismicio/client").Content.${Hero}Slice}
	 */
	export let slice;
</script>

<header class="bg-white dark:bg-gray-900">
	<div class="container px-6 py-16 mx-auto">
		<div class="items-center lg:flex">
			<div class="w-full lg:w-1/2">
				<div class="lg:max-w-lg">
					<p>{slice.primary.eyebrowHeadline}</p>
					<h1 class="text-3xl font-semibold text-gray-800 dark:text-white lg:text-4xl">
						<PrismicRichText field={slice.primary.title} />
					</h1>

					<p class="mt-3 text-gray-600 dark:text-gray-400">
						<PrismicRichText field={slice.primary.description} />
					</p>

					<button
						class="w-full px-5 py-2 mt-6 text-sm tracking-wider text-white uppercase transition-colors duration-300 transform bg-blue-600 rounded-lg lg:w-auto hover:bg-blue-500 focus:outline-none focus:bg-blue-500"
						><PrismicLink field={slice.primary.callToActionLink} class="es-call-to-action__link">
							{slice.primary.callToActionLabel || 'Learn more…'}
						</PrismicLink></button
					>
				</div>
			</div>

			<div class="flex items-center justify-center w-full mt-6 lg:mt-0 lg:w-1/2">
				<PrismicImage field={slice.primary.image} />
			</div>
		</div>
	</div>
</header>
