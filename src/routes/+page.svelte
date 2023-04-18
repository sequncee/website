<script>
	// import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	// @ts-ignore
	import FadeInText from './FadeInText.svelte';


</script>


<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


	<FadeInText text="你 所 能 取 得 的 成 就 没 有 界 限 ，除 非 你 自 己 设 限 。" />
<section>
<!-- generate a section animation -->
	<section class="hero">
		<div class="hero-content">
		  <h1>Welcome to Sequnce E</h1>
		  <p>We are a leading technology company specializing in software development, data analytics, and artificial intelligence.</p>
		  <a href="/about" class="button">Learn More</a>
		</div>
	  </section>
	  <!-- App.svelte -->
  
	  <section class="about">
		<h2>About Us</h2>
		<p>Sequnce E is a technology company that provides a wide range of services to help businesses achieve their goals. Our team of experts specializes in software development, data analytics, and artificial intelligence. We are committed to delivering innovative solutions that help our clients stay ahead of the competition.</p>
		<p>At Sequnce E, we believe in building long-term relationships with our clients. We work closely with them to understand their needs and develop customized solutions that meet their specific requirements. Our goal is to help our clients achieve success by leveraging the latest technologies and best practices.</p>
		<a href="/services" class="button">Our Services</a>
	  </section>
	  
	  <section class="features">
		<h2>Why Choose Sequnce E</h2>
		<div class="feature">
		  <img src="https://via.placeholder.com/150" alt="Feature Image">
		  <h3>Expertise</h3>
		  <p>Our team of experts has years of experience in software development, data analytics, and artificial intelligence.</p>
		</div>
		<div class="feature">
		  <img src="https://via.placeholder.com/150" alt="Feature Image">
		  <h3>Innovation</h3>
		  <p>We are committed to staying ahead of the curve by leveraging the latest technologies and best practices.</p>
		</div>
		<div class="feature">
		  <img src="https://via.placeholder.com/150" alt="Feature Image">
		  <h3>Collaboration</h3>
		  <p>We work closely with our clients to understand their needs and develop customized solutions that meet their specific requirements.</p>
		</div>
	  </section>
	<!-- <Counter /> -->
</section>

<style>


</style>
