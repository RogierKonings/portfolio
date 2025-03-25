<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import Header from './Header.svelte';
	import '../app.css';
	import Navigation from './Navigation.svelte';

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="min-h-screen bg-gray-50">
		<Navigation />
		<main>
			{@render children()}
		</main>
		<footer class="bg-white mt-12">
			<div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
				<div class="text-center">
					<p class="text-gray-500 text-sm">
						© {new Date().getFullYear()} SEO Expert. All rights reserved.
					</p>
				</div>
			</div>
		</footer>
	</div>
</ParaglideJS>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
