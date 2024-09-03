<script>
	import '../app.css';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import { ModeWatcher } from 'mode-watcher';
</script>

<ModeWatcher defaultMode="light" />

<div class="h-screen w-full">
	<Header />
	<slot></slot>
	<Footer />
</div>
