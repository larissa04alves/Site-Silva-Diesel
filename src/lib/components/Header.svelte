<script>
	import { Phone } from 'lucide-svelte';
	import Button from './ui/button/button.svelte';
	let scrollY = 0;
</script>

<svelte:window bind:scrollY />
<nav
	class="fixed z-20 flex h-16 w-full items-center justify-between bg-gradient-to-b {scrollY >
	1.8181817531585693
		? 'from-zinc-900 from-40% to-transparent'
		: ''}"
>
	<!-- <h1 class="fixed right-40 top-40 z-20 bg-white text-5xl text-black">{scrollY}</h1> -->

	<div class="fixed z-10 flex w-full items-center justify-around py-5 text-white">
		<div class="flex items-center">
			<h1 class="staatliches text-4xl">Silva Diesel</h1>
		</div>
		<div class="flex gap-12 text-lg">
			<div
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100"
			>
				<a class="" href="/">Home</a>
			</div>
			<div
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100"
			>
				<a class="" href="/">Sobre</a>
			</div>
			<div
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100"
			>
				<a class="" href="/">Especialidades</a>
			</div>
			<div
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100"
			>
				<a class="" href="/">Endereço</a>
			</div>
		</div>
		<Button
			variant="ghost"
			class="border-[0.05rem] border-white backdrop-blur-3xl hover:border-[#28364e] hover:bg-[#28364e] hover:text-white "
		>
			<span class="relative flex items-center justify-center gap-2">
				<Phone size="18" />(55) 3744-2611</span
			>
		</Button>
	</div>
</nav>
