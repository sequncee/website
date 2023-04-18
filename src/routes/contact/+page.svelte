<svelte:head>
	<title>contact</title>
	<meta name="description" content="About this app" />
</svelte:head>
<section class="contact">
	<h2>Contact Us</h2>
	<p>If you have any questions or would like to learn more about our services, please don't hesitate to contact us.</p>
	<form>
	  <label for="name">Name:</label>
	  <input type="text" id="name" name="name" required>
	  <label for="email">Email:</label>
	  <input type="email" id="email" name="email" required>
	  <label for="message">Message:</label>
	  <textarea id="message" name="message" required></textarea>
	  <button type="submit">Send</button>
	</form>
  </section>