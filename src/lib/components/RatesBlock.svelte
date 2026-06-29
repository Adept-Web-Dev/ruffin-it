<script lang="ts">
	import BlockWrapper from './BlockWrapper.svelte';

	type RateCard = {
		title: string;
		price: string;
		description?: string;
		details?: string[];
	};

	type Props = {
		cards: RateCard[];
		class?: string;
		wrapperClass?: string;
		containerClass?: string;
	};

	let { cards, class: className = '', wrapperClass = '', containerClass = '' }: Props = $props();
</script>

<BlockWrapper class={wrapperClass} {containerClass}>
	<div class={`grid gap-6 md:grid-cols-2 xl:grid-cols-4 ${className}`}>
		{#each cards as card (card.title)}
			<article class="rounded-2xl border border-stone-200 bg-white p-6 shadow-sm">
				<div class="space-y-3">
					<h2 class="text-xl font-semibold text-stone-950">{card.title}</h2>
					<p class="text-3xl font-bold text-stone-950">{card.price}</p>
					{#if card.description}
						<p class="text-stone-700">{card.description}</p>
					{/if}
				</div>

				{#if card.details}
					<ul class="mt-6 space-y-2 text-stone-700">
						{#each card.details as detail (detail)}
							<li>{detail}</li>
						{/each}
					</ul>
				{/if}
			</article>
		{/each}
	</div>
</BlockWrapper>
