<script lang="ts">
	import { onMount } from 'svelte';
	import '../styles/home.css';

	const benefits = [
		{
			title: 'Increased Efficiency',
			description: 'Reduce manual tasks by up to 80% with our intelligent automation solutions',
			icon: '⚡'
		},
		{
			title: 'Cost Savings',
			description: 'Cut operational costs by automating repetitive business processes',
			icon: '💰'
		},
		{
			title: 'Error Reduction',
			description: 'Minimize human errors and ensure consistent results',
			icon: '✅'
		}
	];

	const examples = [
		{
			title: 'Document Processing',
			description: 'Automated invoice processing and data extraction',
			image: '/images/document-automation.jpg'
		},
		{
			title: 'Workflow Automation',
			description: 'Streamlined approval processes and task management',
			image: '/images/workflow-automation.jpg'
		},
		{
			title: 'Data Integration',
			description: 'Seamless connection between your business systems',
			image: '/images/data-integration.jpg'
		}
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="home-container">
	<!-- Hero Section -->
	<section class="section section-alt hero-section">
		<div class="container">
			<h1 class="hero-title">Transform Your Business with Intelligent Automation</h1>
			<p class="hero-description">
				Streamline operations, reduce costs, and boost productivity with our enterprise automation
				solutions
			</p>
			<a href="/services" class="btn btn-primary">Explore Solutions</a>
		</div>
	</section>

	<!-- Benefits Section -->
	<section class="section section-alt">
		<div class="container">
			<h2 class="section-title">Why Choose Our Automation Solutions?</h2>
			<div class="benefits-grid">
				{#each benefits as benefit}
					<div class="benefit-card">
						<div class="benefit-icon">{benefit.icon}</div>
						<h3 class="benefit-title">{benefit.title}</h3>
						<p class="benefit-description">{benefit.description}</p>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- Examples Section -->
	<section class="section">
		<div class="container">
			<h2 class="section-title">Automation in Action</h2>
			<div class="examples-grid">
				{#each examples as example}
					<div class="example-card">
						<img
							src={example.image}
							alt={example.title}
							class="example-image"
						/>
						<div class="example-content">
							<h3 class="example-title">{example.title}</h3>
							<p class="example-description">{example.description}</p>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- CTA Section -->
	<section class="cta-section">
		<div class="container">
			<h2 class="cta-title">Ready to Transform Your Business?</h2>
			<p class="cta-description">
				Join hundreds of businesses that have already automated their operations
			</p>
			<div>
				<a href="/contact" class="btn btn-light">Get Started Today</a>
			</div>
		</div>
	</section>
</div>
