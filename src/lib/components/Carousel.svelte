<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import * as Carousel from '$lib/components/ui/carousel/index.js';

	import oficina from '$lib/img/oficina.webp';
	import concerto from '$lib/img/conserto.webp';
	import concerto2 from '$lib/img/conserto2.webp';
	import concerto3 from '$lib/img/conserto3.webp';
	import total from '$lib/img/total.webp';
	import estoque from '$lib/img/estoque.webp';

	const images = [oficina, concerto, total, concerto2, concerto3, estoque];
</script>

<Carousel.Root
	opts={{
		align: 'start',
		loop: true
	}}
	class="w-screen max-w-7xl"
>
	<Carousel.Content>
		{#each images as image, i (i)}
			<Carousel.Item class="lg:basis-1/3">
				<div>
					<Card.Root>
						<Card.Content class="flex aspect-square items-center justify-center p-0 ">
							<img
								loading="lazy"
								src={image}
								alt={`Imagem ${i + 1}`}
								class="h-full w-full rounded-lg object-cover"
							/>
						</Card.Content>
					</Card.Root>
				</div>
			</Carousel.Item>
		{/each}
	</Carousel.Content>
	<Carousel.Previous />
	<Carousel.Next />
</Carousel.Root>
