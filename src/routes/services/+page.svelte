<script lang="ts">
	const services = [
		{
			name: 'Basic SEO Audit',
			price: '€499',
			description: 'Comprehensive website analysis with actionable recommendations',
			features: [
				'Technical SEO audit',
				'On-page optimization review',
				'Competitor analysis',
				'Basic keyword research',
				'Detailed report with recommendations'
			]
		},
		{
			name: 'Advanced SEO Package',
			price: '€999',
			description: 'Complete SEO optimization with ongoing support',
			features: [
				'Everything in Basic SEO Audit',
				'Content optimization',
				'Advanced keyword research',
				'Link building strategy',
				'3 months of support',
				'Monthly performance reports'
			]
		},
		{
			name: 'Enterprise SEO Solution',
			price: 'Custom',
			description: 'Tailored SEO strategy for large businesses',
			features: [
				'Everything in Advanced SEO Package',
				'Custom SEO strategy',
				'Dedicated SEO manager',
				'Advanced technical optimization',
				'International SEO setup',
				'Ongoing optimization',
				'Quarterly strategy reviews'
			]
		}
	];
</script>

<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
	<div class="text-center">
		<h1 class="text-4xl font-bold text-gray-900 sm:text-5xl">SEO Services & Pricing</h1>
		<p class="mt-4 text-xl text-gray-600">Choose the perfect SEO package for your business</p>
	</div>

	<div class="mt-12 grid gap-8 lg:grid-cols-3">
		{#each services as service}
			<div class="bg-white rounded-lg shadow-lg overflow-hidden">
				<div class="px-6 py-8">
					<h3 class="text-2xl font-bold text-gray-900">{service.name}</h3>
					<p class="mt-4 text-gray-500">{service.description}</p>
					<p class="mt-8">
						<span class="text-4xl font-bold text-gray-900">{service.price}</span>
					</p>
					<a
						href="/contact"
						class="mt-8 block w-full bg-blue-600 text-white text-center py-3 px-6 rounded-md hover:bg-blue-700"
					>
						Get Started
					</a>
				</div>
				<div class="px-6 py-8 bg-gray-50">
					<ul class="space-y-4">
						{#each service.features as feature}
							<li class="flex items-center">
								<svg
									class="h-5 w-5 text-green-500"
									xmlns="http://www.w3.org/2000/svg"
									viewBox="0 0 20 20"
									fill="currentColor"
								>
									<path
										fill-rule="evenodd"
										d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
										clip-rule="evenodd"
									/>
								</svg>
								<span class="ml-3 text-gray-700">{feature}</span>
							</li>
						{/each}
					</ul>
				</div>
			</div>
		{/each}
	</div>

	<div class="mt-16 text-center">
		<h2 class="text-2xl font-bold text-gray-900">Need a Custom Solution?</h2>
		<p class="mt-4 text-gray-600">
			We can create a tailored SEO strategy that perfectly fits your business needs.
		</p>
		<a
			href="/contact"
			class="mt-8 inline-block bg-blue-600 text-white py-3 px-8 rounded-md hover:bg-blue-700"
		>
			Contact Us
		</a>
	</div>
</div>
