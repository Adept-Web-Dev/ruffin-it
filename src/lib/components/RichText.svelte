<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		children?: Snippet;
		class?: string;
	};

	let { children, class: className = '' }: Props = $props();
</script>

<div class={`prose prose-stone lg:prose-lg xl:prose-xl lg:px-8 ${className}`}>
	{#if children}
		{@render children()}
	{/if}
</div>
