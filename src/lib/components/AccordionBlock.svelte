<script lang="ts">
	import { Accordion } from 'bits-ui';
	import BlockWrapper from './BlockWrapper.svelte';
	import RichText from './RichText.svelte';

	type AccordionItem = {
		question: string;
		answer?: string[];
		items?: string[];
		placeholder?: string;
	};

	type Props = {
		items: AccordionItem[];
		class?: string;
		wrapperClass?: string;
		containerClass?: string;
	};

	let { items, class: className = '', wrapperClass = '', containerClass = '' }: Props = $props();
</script>

<BlockWrapper class={wrapperClass} {containerClass}>
	<Accordion.Root
		type="single"
		class={`divide-y divide-stone-200 rounded-2xl border border-stone-200 bg-white shadow-sm ${className}`}
	>
		{#each items as item, index (item.question)}
			<Accordion.Item value={`item-${index}`} class="px-5 sm:px-6">
				<Accordion.Header level={2}>
					<Accordion.Trigger
						class="flex w-full items-center justify-between gap-4 py-5 text-left font-semibold text-stone-950 hover:text-stone-700"
					>
						<span>{item.question}</span>
						<span aria-hidden="true" class="text-2xl leading-none text-stone-500">+</span>
					</Accordion.Trigger>
				</Accordion.Header>
				<Accordion.Content class="pb-5">
					<RichText class={item.placeholder ? 'text-red-600' : ''}>
						{#if item.placeholder}
							<p>{item.placeholder}</p>
						{/if}
						{#if item.answer}
							{#each item.answer as paragraph (paragraph)}
								<p>{paragraph}</p>
							{/each}
						{/if}
						{#if item.items}
							<ul>
								{#each item.items as listItem (listItem)}
									<li>{listItem}</li>
								{/each}
							</ul>
						{/if}
					</RichText>
				</Accordion.Content>
			</Accordion.Item>
		{/each}
	</Accordion.Root>
</BlockWrapper>
