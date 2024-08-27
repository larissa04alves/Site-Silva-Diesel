<script>
	import bgPrincipal from '$lib/img/bg-principal.png';
	import CardBackgroundShine from '$lib/components/animation/CardBackgroundShine.svelte';
	import { Clock8, MapPin, Phone, Pin } from 'lucide-svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import Cards from '$lib/components/Cards.svelte';
	import Marquee from '$lib/components/MarqueeMarcas.svelte';
</script>

<section class="relative flex h-full min-h-full w-full flex-col items-start justify-center">
	<img
		loading="eager"
		class="absolute top-0 flex h-screen w-full"
		src={bgPrincipal}
		alt="hero page"
	/>
	<div class="absolute left-44">
		<CardBackgroundShine />
	</div>
</section>

<section class="flex w-full items-center justify-around bg-[#28364e] py-20">
	<div class="flex items-center gap-4">
		<Clock8 size="55" color="white" />
		<div class="text-white">
			<p>Horário de funcionamento:</p>
			<h1 class="text-2xl font-medium">SEG - SEX: 8:00 - 18:00</h1>
		</div>
	</div>
	<div class="flex items-center gap-4">
		<Phone size="55" color="white" />
		<div class="text-white">
			<p>Entre em contato:</p>
			<h1 class="text-2xl font-medium">(55) 3744-2611</h1>
		</div>
	</div>
	<div class="flex items-center gap-4">
		<MapPin size="55" color="white" />
		<div class="text-white">
			<p>Localização:</p>
			<h1 class="text-2xl font-medium">BR 386 - km 38</h1>
			<h1 class="text-2xl font-medium">F. Westphalen - RS</h1>
		</div>
	</div>
</section>

<section class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-20">
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Especialidades</h1>
	</div>
	<Cards />
</section>

<section class="flex w-full flex-col items-center justify-center gap-10 bg-[#28364e] py-20">
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Marcas Especialistas</h1>
	</div>
	<Marquee />
</section>
