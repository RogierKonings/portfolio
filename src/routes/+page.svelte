<script lang="ts">
  import { onMount } from 'svelte';
  
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

<div class="pt-16">
  <!-- Hero Section -->
  <section class="bg-gradient-to-r from-blue-600 to-blue-800 text-white py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Transform Your Business with Intelligent Automation</h1>
        <p class="text-xl mb-8">Streamline operations, reduce costs, and boost productivity with our enterprise automation solutions</p>
        <a href="/services" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-50 transition">
          Explore Solutions
        </a>
      </div>
    </div>
  </section>

  <!-- Benefits Section -->
  <section class="py-16 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-center mb-12">Why Choose Our Automation Solutions?</h2>
      <div class="grid md:grid-cols-3 gap-8">
        {#each benefits as benefit}
          <div class="bg-white p-6 rounded-lg shadow-md">
            <div class="text-4xl mb-4">{benefit.icon}</div>
            <h3 class="text-xl font-semibold mb-2">{benefit.title}</h3>
            <p class="text-gray-600">{benefit.description}</p>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- Examples Section -->
  <section class="py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-center mb-12">Automation in Action</h2>
      <div class="grid md:grid-cols-3 gap-8">
        {#each examples as example}
          <div class="bg-white rounded-lg shadow-md overflow-hidden">
            <img src={example.image} alt={example.title} class="w-full h-48 object-cover" />
            <div class="p-6">
              <h3 class="text-xl font-semibold mb-2">{example.title}</h3>
              <p class="text-gray-600">{example.description}</p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="bg-blue-600 text-white py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <h2 class="text-3xl font-bold mb-6">Ready to Automate Your Business?</h2>
      <p class="text-xl mb-8">Get started with our automation solutions today</p>
      <div class="space-x-4">
        <a href="/services" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-50 transition">
          View Pricing
        </a>
        <a href="/contact" class="border-2 border-white text-white px-8 py-3 rounded-full font-semibold hover:bg-blue-700 transition">
          Contact Us
        </a>
      </div>
    </div>
  </section>
</div>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 0.6;
  }

  h1 {
    width: 100%;
  }
</style>
