<script lang="ts">
	import bgPrincipal from '$lib/img/bg-principal.webp';
	import bgMobile from '$lib/img/fulltruck.webp';
	import { onMount } from 'svelte';

	import CardBackgroundShine from '$lib/components/animation/CardBackgroundShine.svelte';
	import {
		BadgeCheck,
		Clock8,
		Gauge,
		MapPin,
		Phone,
		SquareActivity,
		UserRoundCheck
	} from 'lucide-svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import Cards from '$lib/components/Cards.svelte';
	import Marquee from '$lib/components/animation/Marquee.svelte';
	import Carousel from '$lib/components/Carousel.svelte';
	import mapa from '$lib/img/mapa.webp';
	import CardMaps from '$lib/components/CardMaps.svelte';
	import mapaMobile from '$lib/img/mapaMobile.webp';

	let isMobile: boolean;
	let currentBg: string;
	let currentMapa: string;

	function checkIfMobile() {
		isMobile = window.innerWidth <= 768; // Define o breakpoint para mobile
		currentBg = isMobile ? bgMobile : bgPrincipal;
		currentMapa = isMobile ? mapaMobile : mapa;
	}

	// Verifica se é mobile no momento da montagem do componente
	onMount(() => {
		checkIfMobile();
		window.addEventListener('resize', checkIfMobile);

		// Remove o event listener quando o componente for destruído
		return () => {
			window.removeEventListener('resize', checkIfMobile);
		};
	});
</script>

<section
	class="relative flex h-full min-h-full w-full flex-col items-start justify-end py-28 md:justify-center"
>
	<img
		loading="eager"
		class="absolute top-0 flex h-[99%] w-full object-cover md:h-screen md:object-fill"
		src={currentBg}
		alt="hero page"
	/>
	<div class="absolute px-5 md:left-44">
		<CardBackgroundShine />
	</div>
</section>

<section class="flex w-full items-center justify-around bg-[#28364e] py-10 md:py-20">
	<div class="hidden items-center gap-4 md:flex">
		<Clock8 color="white" size={55} class="w-8 md:w-20" />
		<div class="text-white">
			<p>Horário de funcionamento:</p>
			<h1 class="font-medium md:text-2xl">SEG - SEX: 8:00 - 18:00</h1>
		</div>
	</div>
	<div class="flex items-center gap-2 md:gap-4">
		<Phone size={55} class="w-8 md:w-20" color="white" />
		<div class="text-white">
			<p>Entre em contato:</p>
			<h1 class="font-medium md:text-2xl">(55) 3744-2611</h1>
		</div>
	</div>
	<div class="flex items-center gap-2 md:gap-4">
		<MapPin size={55} class="w-8 md:w-20" color="white" />
		<div class="text-white">
			<p>Localização:</p>
			<h1 class="font-medium md:text-2xl">BR 386 - km 38</h1>
			<h1 class="font-medium md:text-2xl">F. Westphalen - RS</h1>
		</div>
	</div>
</section>

<section
	id="sobre"
	class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-16 text-white md:py-20"
>
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Diferenciais</h1>
	</div>
	<div class="flex flex-col items-center justify-center md:w-[75%] md:flex-row">
		<div class=" flex h-80 w-full px-3 md:h-56 md:px-0">
			<div class="flex w-1/2 flex-col items-center justify-center gap-3 text-center">
				<BadgeCheck size="70" class="w-14 md:w-20" />
				<h1 class="text-lg font-semibold md:text-xl">Experiência Comprovada</h1>
				<p>
					Possui três décadas de expertise em injeção eletrônica Diesel, atendemos veículos variados
					diesel.
				</p>
			</div>
			<Separator orientation="vertical" class=" mx-3 min-h-[89%]" />
			<div class="flex w-1/2 flex-col items-center justify-center gap-3 text-center">
				<SquareActivity size="70" class="w-14 md:w-20" />
				<h1 class="text-lg font-semibold md:text-xl">Tecnologia Avançada</h1>
				<p>Utilizamos diagnósticos modernos e multimarcas para soluções rápidas e precisas.</p>
			</div>
			<Separator orientation="vertical" class="mx-3 hidden min-h-[89%] md:flex" />
		</div>
		<Separator orientation="horizontal" class="my-4 flex w-[90%] md:hidden" />
		<div class=" flex h-80 w-full px-3 md:h-56 md:px-0">
			<div class="flex w-1/2 flex-col items-center justify-center gap-3 text-center">
				<UserRoundCheck size="70" class="w-14 md:w-20" />
				<h1 class="text-lg font-semibold md:text-xl">Profissionais Qualificados</h1>
				<p>Equipe constantemente atualizada em mecatrônica para serviços seguros e eficazes.</p>
			</div>
			<Separator orientation="vertical" class=" mx-3 min-h-[89%]" />
			<div class="flex w-1/2 flex-col items-center justify-center gap-3 text-center">
				<Gauge size="70" class="w-14 md:w-20" />
				<h1 class="text-lg font-semibold md:text-xl">Cuidado com o Desempenho</h1>
				<p>
					Garantimos manutenção especializada para desempenho ideal de todos os veículos atendidos.
				</p>
			</div>
		</div>
	</div>
</section>

<section
	id="especialidades"
	class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-16 md:py-20"
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

<section class="flex w-full flex-col items-center justify-center gap-10 bg-zinc-900 py-16 md:py-24">
	<div class="flex items-center gap-2">
		<Separator
			orientation="vertical"
			class="h-[3.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
		/>
		<h1 class="staatliches text-5xl text-white">Galeria</h1>
	</div>
	<div class="flex w-full justify-center px-4 md:px-0">
		<Carousel />
	</div>
</section>

<section id="endereco" class="flex w-full flex-col items-center justify-end md:flex-row">
	<a target="_blank" href="https://maps.app.goo.gl/qZQNJPo1G5pnLHAU7">
		<img
			class="relative flex w-full rounded-3xl px-4 md:rounded-none md:px-0"
			src={currentMapa}
			alt="localização"
		/>
	</a>
	<div class="w-full px-4 py-4 md:absolute md:mr-56 md:w-[30%]">
		<CardMaps />
	</div>
</section>
