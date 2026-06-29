<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import { Footer, Nav } from '$lib';

	let { children } = $props();
</script>

<svelte:head>
	<meta name="robots" content="noindex, nofollow" />
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="flex min-h-dvh flex-col bg-stone-50 text-stone-900">
	<Nav />
	<main class="flex-1 space-y-12 pb-12 sm:space-y-16 sm:pb-16">
		{@render children()}
	</main>
	<Footer />
</div>
