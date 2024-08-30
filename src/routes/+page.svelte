<script>
	import bgPrincipal from '$lib/img/bg-principal.webp';
	import CardBackgroundShine from '$lib/components/animation/CardBackgroundShine.svelte';
	import {
		BadgeCheck,
		Clock8,
		Gauge,
		MapPin,
		Phone,
		ScanEye,
		SquareActivity,
		UserRoundCheck
	} from 'lucide-svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import Cards from '$lib/components/Cards.svelte';
	import Marquee from '$lib/components/animation/Marquee.svelte';
	import Carousel from '$lib/components/Carousel.svelte';
	import mapa from '$lib/img/mapa.webp';
	import CardMaps from '$lib/components/CardMaps.svelte';
</script>

<section
	class="relative flex h-full min-h-full w-full flex-col items-start justify-center bg-zinc-900"
>
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

<section
	id="sobre"
	class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-20 text-white"
>
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Diferenciais</h1>
	</div>
	<div class="flex w-[75%] gap-8">
		<div class="flex flex-col items-center justify-center gap-3 text-center">
			<BadgeCheck size="70" />
			<h1 class="text-xl font-semibold">Experiência Comprovada</h1>
			<p>
				Possui três décadas de expertise em injeção eletrônica Diesel, atendemos veículos variados
				diesel.
			</p>
		</div>
		<Separator orientation="vertical" />
		<div class="flex flex-col items-center justify-center gap-3 text-center">
			<SquareActivity size="70" />
			<h1 class="text-xl font-semibold">Tecnologia Avançada</h1>
			<p>Utilizamos diagnósticos modernos e multimarcas para soluções rápidas e precisas.</p>
		</div>
		<Separator orientation="vertical" />
		<div class="flex flex-col items-center justify-center gap-3 text-center">
			<UserRoundCheck size="70" />
			<h1 class="text-xl font-semibold">Profissionais Qualificados</h1>
			<p>Equipe constantemente atualizada em mecatrônica para serviços seguros e eficazes.</p>
		</div>
		<Separator orientation="vertical" />
		<div class="flex flex-col items-center justify-center gap-3 text-center">
			<Gauge size="70" />
			<h1 class="text-xl font-semibold">Cuidado com o Desempenho</h1>
			<p>
				Garantimos manutenção especializada para desempenho ideal de todos os veículos atendidos.
			</p>
		</div>
	</div>
</section>

<section
	id="especialidades"
	class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-20"
>
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Especialidades</h1>
	</div>
	<Cards />
</section>

<section class="flex w-full flex-col items-center justify-center gap-10 bg-[#28364e] py-14">
	<Marquee />
</section>

<section class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-24">
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Galeria</h1>
	</div>
	<div>
		<Carousel />
	</div>
</section>

<section id="endereco" class=" flex w-full items-center justify-end">
	<a target="_blank" href="https://maps.app.goo.gl/qZQNJPo1G5pnLHAU7"
		><img class="relative flex w-full" src={mapa} alt="localizaçao" /></a
	>
	<div class="absolute mr-56 w-[30%]">
		<CardMaps />
	</div>
</section>
