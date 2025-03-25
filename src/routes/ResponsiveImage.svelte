<script lang="ts">
	export let src = '';
	export let alt = '';
	export let sources: any[] = [];
	export let sizes = '100vw';
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
