<script lang="ts">
	import type { Picture } from '@sveltejs/enhanced-img';

	type Props = {
		src?: Picture;
		alt?: string;
		width?: number;
		height?: number;
		class?: string;
	};

	let { src, alt = '', width = 600, height = 400, class: className = '' }: Props = $props();

	const fallbackSrc = $derived(`https://placehold.co/${width}x${height}`);
</script>

{#if src}
	<enhanced:img {src} {alt} class={`w-full object-cover ${className}`} />
{:else}
	<img src={fallbackSrc} {alt} {width} {height} class={`w-full object-cover ${className}`} />
{/if}
