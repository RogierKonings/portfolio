<script lang="ts">
	import '../styles/navigation.css';
	// biome-ignore lint/style/useConst: `isMenuOpen` is reassigned when the menu is toggled
	let isMenuOpen = false;
</script>

<nav class="nav">
	<div class="nav-container">
		<div class="nav-content">
			<div class="nav-left">
				<div class="nav-logo">
					<a href="/" class="nav-logo-link">AutomatePro</a>
				</div>
				<div class="nav-links">
					<a href="/" class="nav-link">Home</a>
					<a href="/services" class="nav-link">Products</a>
					<a href="/contact" class="nav-link">Contact</a>
				</div>
			</div>
			<div class="nav-right">
				<a href="/contact" class="get-started-button">Get Started</a>
			</div>
			<div class="mobile-menu-button">
				<button
					on:click={() => (isMenuOpen = !isMenuOpen)}
					class="mobile-button"
					aria-label="Toggle menu"
				>
					<span class="sr-only">Open main menu</span>
					{#if isMenuOpen}
						<svg
							class="menu-icon"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M6 18L18 6M6 6l12 12"
							/>
						</svg>
					{:else}
						<svg
							class="menu-icon"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M4 6h16M4 12h16M4 18h16"
							/>
						</svg>
					{/if}
				</button>
			</div>
		</div>
		
		{#if isMenuOpen}
			<div class="mobile-menu">
				<div class="mobile-nav-links">
					<a href="/" class="mobile-nav-link">Home</a>
					<a href="/services" class="mobile-nav-link">Products</a>
					<a href="/contact" class="mobile-nav-link">Contact</a>
				</div>
			</div>
		{/if}
	</div>
</nav>
