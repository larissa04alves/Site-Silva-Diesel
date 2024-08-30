<script>
	import { Phone } from 'lucide-svelte';
	import Button from './ui/button/button.svelte';
	let scrollY = 0;
	let activeLink = 'Home';
</script>

<svelte:window bind:scrollY />

<nav
	class="fixed z-20 flex h-16 w-full items-center justify-between bg-gradient-to-b {scrollY >
	1.8181817531585693
		? 'from-zinc-900 from-45% to-transparent'
		: ''}"
>
	<div class="fixed z-10 flex w-full items-center justify-around py-5 text-white">
		<div class="flex items-center">
			<h1 class="staatliches text-4xl">Silva Diesel</h1>
		</div>
		<div class="flex gap-12 text-lg">
			<a
				href="/"
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100 {activeLink ===
				'Home'
					? 'after:origin-bottom-left after:scale-x-100'
					: ''}"
				on:click={() => (activeLink = 'Home')}
			>
				Home
			</a>
			<a
				href="#sobre"
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100 {activeLink ===
				'Sobre'
					? 'after:origin-bottom-left after:scale-x-100'
					: ''}"
				on:click={() => (activeLink = 'Sobre')}
			>
				Sobre
			</a>
			<a
				href="#especialidades"
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100 {activeLink ===
				'Especialidades'
					? 'after:origin-bottom-left after:scale-x-100'
					: ''}"
				on:click={() => (activeLink = 'Especialidades')}
			>
				Especialidades
			</a>
			<a
				href="#endereco"
				class="hover: relative after:absolute after:bottom-0 after:left-0 after:h-1 after:w-full after:origin-bottom-right after:scale-x-0 after:bg-[#184898] after:transition-transform after:duration-300 after:ease-in-out hover:after:origin-bottom-left hover:after:scale-x-100 {activeLink ===
				'Endereço'
					? 'after:origin-bottom-left after:scale-x-100'
					: ''}"
				on:click={() => (activeLink = 'Endereço')}
			>
				Endereço
			</a>
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
