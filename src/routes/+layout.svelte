<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css';
	import '../styles/layout.css';
	import Navigation from './Navigation.svelte';

	const { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="app">
		<Navigation />
		<main>
			{@render children()}
		</main>
		<footer class="footer">
			<div class="footer-container">
				<div class="footer-content">
					<p class="footer-text">
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
