<script>
	import '../app.css';
	import PreHeader from '$lib/components/PreHeader.svelte';
	import Header from '$lib/components/Header.svelte';
</script>

<div class="h-full w-full">
	<PreHeader />
	<Header />
	<slot></slot>
</div>
