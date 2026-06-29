<script lang="ts">
	import type { Snippet } from 'svelte';
	import BlockWrapper from './BlockWrapper.svelte';

	type Props = {
		details?: Snippet;
		form?: Snippet;
		detailsClass?: string;
		formClass?: string;
		wrapperClass?: string;
		containerClass?: string;
	};

	let {
		details,
		form,
		detailsClass = '',
		formClass = '',
		wrapperClass = '',
		containerClass = ''
	}: Props = $props();
</script>

<BlockWrapper class={wrapperClass} containerClass={`grid gap-8 lg:grid-cols-2 ${containerClass}`}>
	{#if details}
		<div
			class={`rounded-2xl border border-stone-200 bg-white p-6 shadow-sm sm:p-8 ${detailsClass}`}
		>
			{@render details()}
		</div>
	{/if}

	{#if form}
		<div class={`rounded-2xl border border-stone-200 bg-white p-6 shadow-sm sm:p-8 ${formClass}`}>
			{@render form()}
		</div>
	{/if}
</BlockWrapper>
