<script lang="ts">
	import * as Card from '$lib/components/ui/card';
	import { Separator } from './ui/separator';
</script>

<Card.Root class=" ">
	<Card.Content class="flex flex-col gap-3 p-5 ">
		<div class="flex flex-col gap-1">
			<div class="flex items-center gap-2">
				<Separator
					orientation="vertical"
					class="h-[2.5rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
				/>
				<h1 class="staatliches text-3xl">Endereço</h1>
			</div>
			<p class="pl-4">BR 386 - km 38, Frederico Westphalen - RS</p>
		</div>
		<Separator />
		<div class="flex flex-col gap-1">
			<div class="flex items-center gap-2">
				<Separator
					orientation="vertical"
					class="h-[2rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
				/>
				<h1 class="staatliches text-3xl">Telefone</h1>
			</div>
			<p class="pl-4">(55) 3744-2611</p>
			<p class="pl-4">(55) 98431-3863</p>
		</div>
		<Separator />
		<div class="flex flex-col gap-1">
			<div class="flex items-center gap-2">
				<Separator
					orientation="vertical"
					class="h-[2rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
				/>
				<h1 class="staatliches text-3xl">E-mail</h1>
			</div>
			<p class="pl-4">eletricajsilva@yahoo.com.br</p>
		</div>
		<Separator />
		<div class="flex flex-col gap-1">
			<div class="flex items-center gap-2">
				<Separator
					orientation="vertical"
					class="h-[2rem] min-h-[2rem] w-[0.4rem] rounded-l-md bg-[#184898]"
				/>
				<h1 class="staatliches text-3xl">Horário</h1>
			</div>
			<p class="pl-4">Seg a sex - 8:00 - 18:00</p>
		</div>
	</Card.Content>
</Card.Root>
