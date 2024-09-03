<script>
	import { Facebook, Instagram, MailCheck, MapPinnedIcon, PhoneForwarded } from 'lucide-svelte';
	import whatsapp from '$lib/img/whatsapp.svg';
</script>

<footer
	class="flex w-full flex-col items-center justify-center gap-4 bg-[#28364e] py-10 md:flex-row md:justify-evenly md:gap-0"
>
	<div
		class="flex flex-col items-center justify-center gap-2 text-white md:items-start md:justify-start"
	>
		<h1 class="staatliches text-5xl">Silva Diesel</h1>
		<p class="text-[15px]">CNPJ: 20.506.848/0001-02</p>
		<div class=" md: flex justify-center gap-2 py-3">
			<a target="_blank" href="https://www.instagram.com/silva_diesel.fw/"
				><Instagram size="35" strokeWidth="1.8" color="white" /></a
			>
			<a target="_blank" href="https://www.facebook.com/p/Silva-Diesel-100064268430043/"
				><Facebook size="35" strokeWidth="1.8" color="white" /></a
			>
			<a target="_blank" href="https://wa.me/5555984313863?text=Ol%C3%A1!%20Tudo%20bem%3F%20"
				><img loading="lazy" class="" src={whatsapp} alt="whatsapp" /></a
			>
		</div>
	</div>
	<div class="flex gap-6 px-4 md:gap-40">
		<div class="flex flex-col gap-1 text-white">
			<h1 class="staatliches text-2xl">Especialidades</h1>
			<div class="text-[15px]">
				<p>Linha diesel leve e pesada</p>
				<p>Sistema de bicos injetores</p>
				<p>Conserto e programação de módulos</p>
				<p>Sistema de arla</p>
			</div>
		</div>
		<div class="flex flex-col text-white">
			<h1 class="staatliches text-2xl">Horários</h1>
			<div class="text-[15px]">
				<p>Seg-Sex: 8:00 - 18:00</p>
				<p class="hidden md:flex">Fechamos ao meio dia</p>
				Sab-Dom: Fechado
			</div>
		</div>
		<div class="hidden flex-col gap-2 text-white md:flex">
			<h1 class="staatliches text-2xl">Localização</h1>
			<div class="flex gap-2 text-[15px]">
				<MapPinnedIcon size="20" />
				<p>BR 386 - km 38, FW - RS</p>
			</div>
			<div class="flex gap-2 text-sm">
				<MailCheck size="20" />
				<p>eletricajsilva@yahoo.com.br</p>
			</div>
			<div class="flex gap-2 text-sm">
				<PhoneForwarded size="20" />
				<p>(55) 3744-2611</p>
			</div>
		</div>
	</div>
</footer>
