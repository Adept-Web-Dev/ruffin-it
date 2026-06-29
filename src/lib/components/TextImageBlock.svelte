<script lang="ts">
	import type { Picture } from '@sveltejs/enhanced-img';
	import type { Snippet } from 'svelte';
	import BlockWrapper from './BlockWrapper.svelte';
	import Image from './Image.svelte';
	import RichText from './RichText.svelte';

	type Props = {
		children?: Snippet;
		imageSrc?: Picture;
		imageAlt?: string;
		imagePosition?: 'left' | 'right';
		class?: string;
		wrapperClass?: string;
		containerClass?: string;
	};

	let {
		children,
		imageSrc,
		imageAlt = '',
		imagePosition = 'right',
		class: className = '',
		wrapperClass = '',
		containerClass = ''
	}: Props = $props();

	const imageOrder = $derived(imagePosition === 'left' ? 'lg:order-first' : 'lg:order-last');
</script>

<BlockWrapper
	class={wrapperClass}
	containerClass={`grid gap-10 lg:grid-cols-2 lg:items-center ${containerClass}`}
>
	<RichText class={`mx-auto ${className}`}>
		{#if children}
			{@render children()}
		{/if}
	</RichText>

	<div class={imageOrder}>
		<Image src={imageSrc} alt={imageAlt} class="aspect-[3/2] rounded-2xl shadow-sm" />
	</div>
</BlockWrapper>
