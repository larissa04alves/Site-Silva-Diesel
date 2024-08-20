<script>
	import '../app.css';
	import Header from '$lib/components/Header.svelte';
</script>

<div class="h-screen w-full">
	<Header />
	<slot></slot>
</div>
