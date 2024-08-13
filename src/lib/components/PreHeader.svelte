<script>
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import Phone from 'lucide-svelte/icons/phone';
	import Clock8 from 'lucide-svelte/icons/clock-8';
	import MapPin from 'lucide-svelte/icons/map-pin';
</script>

<div class="flex w-full justify-between px-20 py-3">
	<div class="flex w-1/2 items-center gap-6">
		<div class="flex flex-col text-[#989898]">
			<div class="flex gap-1">
				<MapPin />
				<h1 class="text-[0.94rem]">Localização</h1>
			</div>
			<p class="pl-7 text-sm">BR 386 km 38</p>
			<p class="pl-7 text-sm">Frederico Westphalen - RS</p>
		</div>
		<Separator orientation="vertical" class="min-h-16 bg-[#CBCBCB]" />
		<div class="flex flex-col text-[#989898]">
			<div class="flex gap-1">
				<Clock8 />
				<h1 class="text-[0.94rem]">Horário</h1>
			</div>
			<p class="pl-7 text-sm">Segunda a sexta</p>
			<p class="pl-7 text-sm">08:00 - 18:00</p>
		</div>
	</div>
	<div class="text-[#989898]">
		<div class="flex flex-col">
			<div class="flex gap-1">
				<Phone />
				<h1 class="text-[0.94rem]">Contato</h1>
			</div>
			<p class="pl-7 text-sm">(55) 98431-3863</p>
			<p class="pl-7 text-sm">(55) 3744-2611</p>
		</div>
	</div>
</div>
<Separator orientation="horizontal" class="bg-[#CBCBCB]" />
