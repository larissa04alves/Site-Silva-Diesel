<script>
	import * as Sheet from '$lib/components/ui/sheet';
	import { Facebook, Instagram, Menu, PhoneForwarded } from 'lucide-svelte';
	import Button from './ui/button/button.svelte';
	import whatsapp from '$lib/img/whatsapp.svg';

	let isOpen = false;

	function toggleSheet() {
		isOpen = !isOpen;
	}
</script>

<nav
	class="fixed z-10 flex w-screen items-center justify-between bg-zinc-900/75 px-6 py-2 backdrop-blur-sm"
>
	<Button href="tel:55984313863" variant="ghost" class="hover:bg-transparent">
		<PhoneForwarded size="30" color="white" />
	</Button>
	<h1 class="staatliches text-3xl text-white">Silva Diesel</h1>
	<div>
		<Sheet.Root bind:open={isOpen}>
			<Sheet.Trigger>
				<Menu size="40" color="white" />
			</Sheet.Trigger>
			<Sheet.Content
				side="left"
				class=" flex flex-col items-center justify-between border-none bg-zinc-900 py-10"
			>
				<Sheet.Header class="flex gap-5">
					<Sheet.Title class="staatliches text-3xl text-white">Silva Diesel</Sheet.Title>
					<Sheet.Description class="flex flex-col ">
						<Button
							href="/"
							on:click={toggleSheet}
							variant="ghost"
							class="text-lg hover:bg-zinc-900 hover:text-white">Home</Button
						>
						<Button
							on:click={toggleSheet}
							href="#sobre"
							variant="ghost"
							class="text-lg hover:bg-zinc-900 hover:text-white">Sobre</Button
						>
						<Button
							href="#especialidades"
							on:click={toggleSheet}
							variant="ghost"
							class="text-lg hover:bg-zinc-900 hover:text-white">Especialidades</Button
						>
						<Button
							href="#endereco"
							on:click={toggleSheet}
							variant="ghost"
							class="text-lg hover:bg-zinc-900 hover:text-white">Endereço</Button
						>
					</Sheet.Description>
				</Sheet.Header>
				<Sheet.Footer>
					<div class="flex gap-2">
						<a target="_blank" href="https://www.instagram.com/silva_diesel.fw/"
							><Instagram size="45" color="white" /></a
						>
						<a target="_blank" href="https://www.facebook.com/p/Silva-Diesel-100064268430043/"
							><Facebook size="45" color="white" /></a
						>
						<a target="_blank" href="https://wa.me/5555984313863?text=Ol%C3%A1!%20Tudo%20bem%3F%20"
							><img class="w-10" src={whatsapp} alt="whatsapp" /></a
						>
					</div>
				</Sheet.Footer>
			</Sheet.Content>
		</Sheet.Root>
	</div>
</nav>
