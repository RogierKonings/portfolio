<script lang="ts">
	import '../../styles/contact.css';

	let formData = {
		name: '',
		email: '',
		company: '',
		package: 'starter',
		message: ''
	};

	const packages = ['starter', 'professional', 'enterprise'];

	function handleSubmit() {
		// Here you would typically handle the form submission
		console.log('Form submitted:', formData);
		// Reset form
		formData = {
			name: '',
			email: '',
			company: '',
			package: 'starter',
			message: ''
		};
	}
</script>

<svelte:head>
	<title>Contact</title>
	<meta name="description" content="Contact Us" />
</svelte:head>

<div class="contact-container">
	<!-- Contact Header -->
	<section class="section">
		<div class="container">
			<div class="contact-grid">
				<!-- Contact Form -->
				<div class="contact-form">
					<h2 class="section-title">Get in Touch</h2>
					<form on:submit|preventDefault={handleSubmit}>
						<div class="form-group">
							<label class="form-label" for="name">Name</label>
							<input type="text" id="name" class="form-input" bind:value={formData.name} required />
						</div>

						<div class="form-group">
							<label class="form-label" for="email">Email</label>
							<input
								type="email"
								id="email"
								class="form-input"
								bind:value={formData.email}
								required
							/>
						</div>

						<div class="form-group">
							<label class="form-label" for="company">Company</label>
							<input
								type="text"
								id="company"
								class="form-input"
								bind:value={formData.company}
								required
							/>
						</div>

						<div class="form-group">
							<label class="form-label" for="package">Interested Package</label>
							<select id="package" class="form-select" bind:value={formData.package}>
								{#each packages as pkg}
									<option value={pkg}>{pkg.charAt(0).toUpperCase() + pkg.slice(1)}</option>
								{/each}
							</select>
						</div>

						<div class="form-group">
							<label class="form-label" for="message">Message</label>
							<textarea
								id="message"
								class="form-textarea"
								rows="4"
								bind:value={formData.message}
								required
							></textarea>
						</div>

						<button type="submit" class="btn btn-primary">Send Message</button>
					</form>
				</div>

				<!-- Contact Information -->
				<div class="contact-info">
					<h2 class="section-title">Contact Information</h2>

					<div class="info-group">
						<h3 class="info-title">Email</h3>
						<p class="info-content">
							<a href="mailto:contact@automatepro.com">contact@automatepro.com</a>
						</p>
					</div>

					<div class="info-group">
						<h3 class="info-title">Phone</h3>
						<p class="info-content">
							<a href="tel:+1234567890">+1 (234) 567-890</a>
						</p>
					</div>

					<div class="info-group">
						<h3 class="info-title">Office</h3>
						<p class="info-content">
							123 Automation Street<br />
							Silicon Valley, CA 94025<br />
							United States
						</p>
					</div>

					<div class="info-group">
						<h3 class="info-title">Hours</h3>
						<p class="info-content">
							Monday - Friday<br />
							9:00 AM - 6:00 PM PST
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>

	<!-- Map Section -->
	<section class="section map-section">
		<div class="container">
			<div class="map-container">
				<iframe
					src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3168.4033560425414!2d-122.08374688397888!3d37.42199997982367!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x808fba02425dad8f%3A0x6c296c66619367e0!2sGoogleplex!5e0!3m2!1sen!2sus!4v1624308999821!5m2!1sen!2sus"
					title="Office Location"
					loading="lazy"
				></iframe>
			</div>
		</div>
	</section>
</div>
