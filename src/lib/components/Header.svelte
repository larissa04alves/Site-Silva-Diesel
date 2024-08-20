<script>
	import { Phone } from 'lucide-svelte';
	import Button from './ui/button/button.svelte';
</script>

<div class="fixed z-10 flex w-full items-center justify-around py-5 text-white">
	<div class="flex items-center">
		<h1 class="staatliches text-4xl">Silva Diesel</h1>
	</div>
	<div class="flex gap-12 text-lg">
		<a class="hover:" href="/">Home</a>
		<a href="#">Sobre</a>
		<a href="#">Serviços</a>
		<a href="#">Endereço</a>
	</div>
	<Button variant="ghost" class="border-[0.05rem] border-white backdrop-blur-3xl ">
		<span class="relative flex items-center justify-center gap-2">
			<Phone size="18" />(55) 3744-2611</span
		>
	</Button>
</div>
