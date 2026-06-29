<script lang="ts">
	import type { Picture } from '@sveltejs/enhanced-img';
	import BlockWrapper from './BlockWrapper.svelte';
	import Image from './Image.svelte';
	import RichText from './RichText.svelte';

	type Props = {
		title: string;
		subtitle?: string;
		class?: string;
		imageSrc?: Picture;
		imageAlt?: string;
	};

	let { title, subtitle, class: className = '', imageSrc, imageAlt = '' }: Props = $props();
</script>

<section class="relative w-full overflow-hidden">
	<Image src={imageSrc} alt={imageAlt} width={1600} height={500} class="h-[420px] sm:h-[520px]" />
	<div class="absolute inset-0 bg-gradient-to-r from-black/65 via-black/35 to-black/10"></div>
	<BlockWrapper as="div" class="absolute inset-0 flex items-center">
		<RichText
			class={`prose-invert mx-auto text-center [text-shadow:0_2px_16px_rgb(0_0_0_/_0.65)] ${className}`}
		>
			<h1>{title}</h1>
			{#if subtitle}
				<h2>({subtitle})</h2>
			{/if}
		</RichText>
	</BlockWrapper>
</section>
