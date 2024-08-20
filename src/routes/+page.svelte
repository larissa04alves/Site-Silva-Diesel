<script>
	import Group from '$lib/img/Group 1.png';
	import CardBackgroundShine from '$lib/components/animation/CardBackgroundShine.svelte';
</script>

<section class="relative flex h-full min-h-full w-full flex-col items-start justify-center">
	<img class="absolute top-0 flex h-screen w-full" src={Group} alt="hero page" />
	<div class="absolute left-44">
		<CardBackgroundShine />
	</div>
</section>
