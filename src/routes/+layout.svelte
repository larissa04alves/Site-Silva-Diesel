<script>
	import '../app.css';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<div class="h-screen w-full">
	<Header />
	<slot></slot>
	<Footer />
</div>
