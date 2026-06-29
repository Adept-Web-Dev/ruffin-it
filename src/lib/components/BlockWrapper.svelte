<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		as?: 'section' | 'div' | 'header' | 'footer';
		children?: Snippet;
		class?: string;
		containerClass?: string;
	};

	let { as = 'section', children, class: className = '', containerClass = '' }: Props = $props();
</script>

<svelte:element this={as} class={`w-full px-4 sm:px-8 ${className}`}>
	<div class={`container mx-auto ${containerClass}`}>
		{#if children}
			{@render children()}
		{/if}
	</div>
</svelte:element>
