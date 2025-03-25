<script lang="ts">
	let formData = {
		name: '',
		email: '',
		phone: '',
		website: '',
		message: '',
		service: 'basic'
	};

	const services = [
		{ value: 'basic', label: 'Basic SEO Audit' },
		{ value: 'advanced', label: 'Advanced SEO Package' },
		{ value: 'enterprise', label: 'Enterprise SEO Solution' }
	];

	function handleSubmit() {
		// Here you would typically send the form data to your backend
		console.log('Form submitted:', formData);
	}
</script>

<svelte:head>
	<title>Contact</title>
	<meta name="description" content="Contact SEO Kings" />
</svelte:head>

<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
	<div class="max-w-3xl mx-auto">
		<div class="text-center">
			<h1 class="text-4xl font-bold text-gray-900 sm:text-5xl">Contact Us</h1>
			<p class="mt-4 text-xl text-gray-600">
				Get in touch with our SEO experts and start improving your website's performance today.
			</p>
		</div>

		<div class="mt-12 grid grid-cols-1 gap-8 lg:grid-cols-2">
			<!-- Contact Information -->
			<div>
				<h2 class="text-2xl font-bold text-gray-900">Get in Touch</h2>
				<p class="mt-4 text-gray-600">
					Ready to improve your website's search engine rankings? Contact us for a free
					consultation.
				</p>

				<div class="mt-8 space-y-6">
					<div class="flex items-center">
						<svg
							class="h-6 w-6 text-blue-600"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
							/>
						</svg>
						<span class="ml-3 text-gray-600">contact@seoexpert.com</span>
					</div>
					<div class="flex items-center">
						<svg
							class="h-6 w-6 text-blue-600"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
							/>
						</svg>
						<span class="ml-3 text-gray-600">+1 (555) 123-4567</span>
					</div>
					<div class="flex items-center">
						<svg
							class="h-6 w-6 text-blue-600"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
							/>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
							/>
						</svg>
						<span class="ml-3 text-gray-600">123 SEO Street, Digital City, 12345</span>
					</div>
				</div>
			</div>

			<!-- Contact Form -->
			<form on:submit|preventDefault={handleSubmit} class="space-y-6">
				<div>
					<label for="name" class="block text-sm font-medium text-gray-700">Name</label>
					<input
						type="text"
						id="name"
						bind:value={formData.name}
						required
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					/>
				</div>

				<div>
					<label for="email" class="block text-sm font-medium text-gray-700">Email</label>
					<input
						type="email"
						id="email"
						bind:value={formData.email}
						required
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					/>
				</div>

				<div>
					<label for="phone" class="block text-sm font-medium text-gray-700">Phone</label>
					<input
						type="tel"
						id="phone"
						bind:value={formData.phone}
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					/>
				</div>

				<div>
					<label for="website" class="block text-sm font-medium text-gray-700">Website</label>
					<input
						type="url"
						id="website"
						bind:value={formData.website}
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					/>
				</div>

				<div>
					<label for="service" class="block text-sm font-medium text-gray-700"
						>Service Interest</label
					>
					<select
						id="service"
						bind:value={formData.service}
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					>
						{#each services as service}
							<option value={service.value}>{service.label}</option>
						{/each}
					</select>
				</div>

				<div>
					<label for="message" class="block text-sm font-medium text-gray-700">Message</label>
					<textarea
						id="message"
						bind:value={formData.message}
						rows="4"
						required
						class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-blue-500 focus:ring-blue-500"
					></textarea>
				</div>

				<div>
					<button
						type="submit"
						class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500"
					>
						Send Message
					</button>
				</div>
			</form>
		</div>
	</div>
</div>
