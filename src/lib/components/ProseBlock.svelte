<script lang="ts">
	import type { Snippet } from 'svelte';
	import BlockWrapper from './BlockWrapper.svelte';
	import RichText from './RichText.svelte';

	type Props = {
		children?: Snippet;
		class?: string;
		wrapperClass?: string;
		containerClass?: string;
	};

	let { children, class: className = '', wrapperClass = '', containerClass = '' }: Props = $props();
</script>

<BlockWrapper class={wrapperClass} {containerClass}>
	<RichText class={`mx-auto ${className}`}>
		{#if children}
			{@render children()}
		{/if}
	</RichText>
</BlockWrapper>
