<script>
	import * as Card from '$lib/components/ui/card';
	import bico from '$lib/img/bico.svg';
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
				'Manutenção especializada em sistemas de alta pressão, com foco em eficiência e segurança, utilizando tecnologia de ponta para otimizar o desempenho do motor diesel.',
			image: bomba,
			alt: 'Chaves de fenda'
		},
		{
			title: 'Reparos de Chicotes Eletrônicos',
			description:
				'Conserto e substituição de chicotes eletrônicos com atenção aos detalhes, garantindo a integridade dos sistemas elétricos para um funcionamento seguro e confiável.',
			image: estrutura,
			alt: 'Chicote eletrônico'
		},
		{
			title: 'Sistema de Arla',
			description:
				'Serviço especializado em sistemas de Arla, assegurando a conformidade com normas ambientais e a máxima eficiência do sistema de controle de emissões.',
			image: arla,
			alt: 'Sistema de Arla'
		},
		{
			title: 'Programação de Módulos',
			description:
				'Programação de módulos eletrônicos com ferramentas avançadas, ajustando parâmetros para melhorar o desempenho, economia de combustível e a longevidade do veículo.',
			image: modulo,
			alt: 'Módulo eletrônico'
		},
		{
			title: 'Diagnósticos Especializados',
			description:
				'Com tecnologia avançada, identificamos falhas rapidamente, possibilitando intervenções precisas que garantem o desempenho ideal e prolongam a vida útil do veículo.',
			image: diagnostic,
			alt: 'Diagnóstico de veículo'
		}
	];
</script>

<div class="grid grid-cols-1 gap-10 md:grid-cols-2 lg:grid-cols-3">
	{#each cards as { title, description, image, alt }, i}
		<Card.Root class="flex max-h-[250px] min-h-[200px] min-w-[350px] max-w-[380px] flex-col">
			<Card.Header class="flex flex-col items-center justify-center">
				<img loading="lazy" class="w-3/12" src={image} {alt} />
				<Card.Title
					class="staatliches bg-gradient-to-b from-[#184898] via-[#28364E] to-[#28364E] bg-clip-text text-2xl tracking-wide text-transparent"
					>{title}</Card.Title
				>
				<Card.Description class="text-center">{description}</Card.Description>
			</Card.Header>
		</Card.Root>
	{/each}
</div>
