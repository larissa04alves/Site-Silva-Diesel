<script lang="ts">
	import { cn } from '$lib/utils';

	import chevrolet from '$lib/img/marcas/chevrolet.svg';
	import daf from '$lib/img/marcas/daf.svg';
	import ford from '$lib/img/marcas/ford.svg';
	import iveco from '$lib/img/marcas/iveco.svg';
	import jeep from '$lib/img/marcas/jeep.svg';
	import mercedes from '$lib/img/marcas/mercedez.svg';
	import mitsubishi from '$lib/img/marcas/mitsubishi.svg';
	import ram from '$lib/img/marcas/ram.svg';
	import scania from '$lib/img/marcas/scania.svg';
	import toyota from '$lib/img/marcas/toyota.svg';
	import volks from '$lib/img/marcas/volks.svg';
	import volvo from '$lib/img/marcas/volvo.svg';

	export let pauseOnHover: boolean = false;
	export let vertical: boolean = false;
	export let repeat: number = 4;
	export let reverse: boolean = false;

	let className: any = '';
	export { className as class };

	const marcas = [
		scania,
		toyota,
		chevrolet,
		volks,
		mitsubishi,
		ford,
		ram,
		volvo,
		jeep,
		mercedes,
		daf,
		iveco,
		toyota
	];
</script>

<div
	class={cn(
		'group flex w-full overflow-hidden p-2 [--duration:12s] [--gap:2rem] [gap:var(--gap)]',
		{
			'flex-row': !vertical,
			'flex-col': vertical
		},
		className
	)}
>
	{#each { length: repeat } as _, i (i)}
		<div
			class={cn('flex shrink-0 justify-around [gap:var(--gap)]', {
				'animate-marquee flex-row': !vertical,
				'animate-marquee-vertical flex-col': vertical,
				'group-hover:[animation-play-state:paused]': pauseOnHover,
				'[animation-direction:reverse]': reverse
			})}
		>
			{#each marcas as marca}
				<img src={marca} alt="Logo" class=" flex h-20" />
			{/each}
		</div>
	{/each}
</div>
