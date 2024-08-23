<script>
	import * as Card from '$lib/components/ui/card';
	import bico from '$lib/img/bico.svg';
	import { Button } from './ui/button';
	import bomba from '$lib/img/bomba.svg';
	import estrutura from '$lib/img/estrutura.svg';
	import arla from '$lib/img/arla.svg';
	import modulo from '$lib/img/modulo.svg';
	import diagnostic from '$lib/img/diagnostic.svg';

	const cards = [
		{
			title: 'Unidades Injetoras',
			description:
				'Diagnóstico preciso e reparo eficiente em sistemas de injeção diesel, utilizando equipamentos modernos para garantir o máximo desempenho e durabilidade do seu motor.',
			image: bico,
			alt: 'Bico injetor'
		},
		{
			title: 'Bomba de Alta Pressão',
			description:
				'Potência constante, alta durabilidade e desempenho ideal para motores de caminhões.',
			image: bomba,
			alt: 'Chaves de fenda'
		},
		{
			title: 'Reparos de Chicotes Eletrônicos',
			description:
				'Restauração completa, garantindo conexão segura e desempenho confiável dos sistemas elétricos.',
			image: estrutura,
			alt: 'Chicote eletrônico'
		},
		{
			title: 'Sistema de Arla',
			description:
				'Eficiente redução de emissões, operação estável e suporte à sustentabilidade em veículos pesados.',
			image: arla,
			alt: 'Sistema de Arla'
		},
		{
			title: 'Programação de Módulos',
			description:
				'Com equipamentos modernos, garantimos ajustes para máximo desempenho do seu veículo.',
			image: modulo,
			alt: 'Módulo eletrônico'
		},
		{
			title: 'Diagnósticos Especializados',
			description:
				'Equipamentos avançados, garantindo análises e soluções eficientes para o seu veículo.',
			image: diagnostic,
			alt: 'Diagnóstico de veículo'
		}
	];
</script>

<div class="grid grid-cols-1 gap-10 md:grid-cols-2 lg:grid-cols-3">
	{#each cards as { title, description, image, alt }, i}
		<Card.Root class="flex max-h-[250px] min-h-[200px] min-w-[350px] max-w-[380px] flex-col">
			<Card.Header class="flex flex-col items-center justify-center">
				<img class="w-3/12" src={image} {alt} />
				<Card.Title
					class="staatliches bg-gradient-to-b from-[#184898] via-[#28364E] to-[#28364E] bg-clip-text text-2xl tracking-wide text-transparent"
					>{title}</Card.Title
				>
				<Card.Description class="text-center">{description}</Card.Description>
			</Card.Header>
		</Card.Root>
	{/each}
</div>
