<script lang="ts">
	interface ImageSource {
		srcset: string;
		media?: string;
		type?: string;
	}

	export const src = '';
	export const alt = '';
	export const sources: ImageSource[] = [];
	export const sizes = '100vw';
</script>

<!-- Responsive Image Component -->
<picture>
	{#each sources as source}
		<source srcset={source.srcset} media={source.media} type={source.type} />
	{/each}
	<enhanced:img {src} {alt} {sizes} loading="lazy" />
</picture>

<style>
	picture,
	img {
		display: block;
		max-width: 100%;
		height: auto;
	}
</style>
