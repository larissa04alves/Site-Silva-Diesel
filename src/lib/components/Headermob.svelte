<script>
	import * as Sheet from '$lib/components/ui/sheet';
	import { Menu, PhoneForwarded } from 'lucide-svelte';
	import Button from './ui/button/button.svelte';
</script>

<nav class="fixed z-10 flex w-screen items-center justify-between px-6 py-2 backdrop-blur-sm">
	<Button variant="ghost">
		<PhoneForwarded size="30" color="white" />
	</Button>
	<h1 class="staatliches text-3xl text-white">Silva Diesel</h1>
	<div>
		<Sheet.Root open>
			<Sheet.Trigger>
				<label class="flex w-8 flex-col gap-2">
					<input class="peer hidden" type="checkbox" />
					<div
						class="h-[3px] w-1/2 origin-right rounded-2xl bg-black duration-500 peer-checked:-translate-x-[12px] peer-checked:-translate-y-[1px] peer-checked:rotate-[225deg]"
					></div>
					<div
						class="h-[3px] w-full rounded-2xl bg-black duration-500 peer-checked:-rotate-45"
					></div>
					<div
						class="h-[3px] w-1/2 origin-left place-self-end rounded-2xl bg-black duration-500 peer-checked:translate-x-[12px] peer-checked:translate-y-[1px] peer-checked:rotate-[225deg]"
					></div>
				</label>
			</Sheet.Trigger>
			<Sheet.Content side="left" class=" bg-zinc-900">
				<Sheet.Header>
					<Sheet.Title class="staatliches text-3xl text-white">Silva Diesel</Sheet.Title>
					<Sheet.Description class="flex flex-col">
						<Button variant="ghost">Home</Button>
						<Button variant="ghost">Sobre</Button>
						<Button variant="ghost">Especialidades</Button>
						<Button variant="ghost">Endereço</Button>
					</Sheet.Description>
				</Sheet.Header>
			</Sheet.Content>
		</Sheet.Root>
	</div>
</nav>
