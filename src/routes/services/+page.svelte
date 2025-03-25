<script lang="ts">
	import '../../styles/services.css';
	
	const packages = [
		{
			name: 'Starter',
			price: '999',
			description: 'Perfect for small businesses starting with automation',
			features: [
				'Document Processing Automation',
				'Basic Workflow Automation',
				'Email Integration',
				'Standard Support',
				'2 Automation Workflows'
			]
		},
		{
			name: 'Professional',
			price: '2,499',
			description: 'Ideal for growing businesses with complex needs',
			features: [
				'Everything in Starter',
				'Advanced Workflow Automation',
				'CRM Integration',
				'Priority Support',
				'5 Automation Workflows',
				'Custom Reporting'
			],
			highlighted: true
		},
		{
			name: 'Enterprise',
			price: 'Custom',
			description: 'For large organizations requiring full-scale automation',
			features: [
				'Everything in Professional',
				'Unlimited Automation Workflows',
				'Custom API Integration',
				'Dedicated Support Manager',
				'Advanced Analytics',
				'Custom Development'
			]
		}
	];
</script>

<div class="services-container">
	<!-- Pricing Header -->
	<section class="section section-alt">
		<div class="pricing-header">
			<h1>Choose Your Automation Package</h1>
			<p class="pricing-description">
				Select the perfect automation solution that fits your business needs and budget
			</p>
		</div>
	</section>

	<!-- Pricing Cards -->
	<section class="section">
		<div class="container">
			<div class="pricing-grid">
				{#each packages as pkg}
					<div class="pricing-card" class:highlighted={pkg.highlighted}>
						{#if pkg.highlighted}
							<div class="highlighted-badge"></div>
						{/if}
						<div class="card-content" class:highlighted={pkg.highlighted}>
							<h3 class="package-name">{pkg.name}</h3>
							<div class="price-container">
								<span class="price">${pkg.price}</span>
								{#if pkg.price !== 'Custom'}
									<span class="price-period">/month</span>
								{/if}
							</div>
							<p class="package-description">
								{pkg.description}
							</p>
						</div>
						<div class="features-container">
							<ul class="features-list">
								{#each pkg.features as feature}
									<li class="feature-item">
										<svg
											class="feature-icon"
											fill="none"
											stroke="currentColor"
											viewBox="0 0 24 24"
										>
											<path
												stroke-linecap="round"
												stroke-linejoin="round"
												stroke-width="2"
												d="M5 13l4 4L19 7"
											/>
										</svg>
										{feature}
									</li>
								{/each}
							</ul>
							<a
								href="/contact"
								class="cta-button"
								class:outlined={!pkg.highlighted}
							>
								{pkg.price === 'Custom' ? 'Contact Us' : 'Get Started'}
							</a>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- FAQ Section -->
	<section class="section section-alt">
		<div class="container">
			<h2 class="faq-title">Frequently Asked Questions</h2>
			<div class="faq-grid">
				<div class="faq-card">
					<h3 class="faq-question">How quickly can I get started?</h3>
					<p class="faq-answer">
						Most automation solutions can be implemented within 2-4 weeks, depending on complexity
						and requirements.
					</p>
				</div>
				<div class="faq-card">
					<h3 class="faq-question">Do you offer custom solutions?</h3>
					<p class="faq-answer">
						Yes, our Enterprise package includes custom development to meet your specific automation
						needs.
					</p>
				</div>
				<div class="faq-card">
					<h3 class="faq-question">What kind of support do you provide?</h3>
					<p class="faq-answer">
						We offer different levels of support based on your package, from standard support to
						dedicated support managers.
					</p>
				</div>
				<div class="faq-card">
					<h3 class="faq-question">Can I upgrade my package later?</h3>
					<p class="faq-answer">
						Yes, you can upgrade to a higher tier package at any time as your automation needs grow.
					</p>
				</div>
			</div>
		</div>
	</section>
</div>

<style>
	/* Add styles here */
</style>
