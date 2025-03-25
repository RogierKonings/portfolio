<script lang="ts">
	const isMenuOpen = false;
</script>

<nav class="bg-white shadow-lg fixed w-full z-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between h-16">
			<div class="flex">
				<div class="flex-shrink-0 flex items-center">
					<a href="/" class="text-xl font-bold text-blue-600">AutomatePro</a>
				</div>
				<div class="hidden sm:ml-6 sm:flex sm:space-x-8">
					<a href="/" class="inline-flex items-center px-1 pt-1 text-gray-700 hover:text-blue-600">Home</a>
					<a href="/services" class="inline-flex items-center px-1 pt-1 text-gray-700 hover:text-blue-600">Products</a>
					<a href="/contact" class="inline-flex items-center px-1 pt-1 text-gray-700 hover:text-blue-600">Contact</a>
				</div>
			</div>
			<div class="hidden sm:ml-6 sm:flex sm:items-center">
				<a
					href="/contact"
					class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700"
				>
					Get Started
				</a>
			</div>
			<div class="-mr-2 flex items-center sm:hidden">
				<button
					on:click={() => (isMenuOpen = !isMenuOpen)}
					class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-blue-500"
				>
					<span class="sr-only">Open main menu</span>
					{#if isMenuOpen}
						<svg
							class="block h-6 w-6"
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
							class="block h-6 w-6"
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
	</div>

	{#if isMenuOpen}
		<div class="sm:hidden">
			<div class="pt-2 pb-3 space-y-1">
				<a
					href="/"
					class="block pl-3 pr-4 py-2 text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
				>
					Home
				</a>
				<a
					href="/services"
					class="block pl-3 pr-4 py-2 text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
				>
					Products
				</a>
				<a
					href="/contact"
					class="block pl-3 pr-4 py-2 text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50"
				>
					Contact
				</a>
			</div>
		</div>
	{/if}
</nav>
