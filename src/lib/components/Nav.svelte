<script lang="ts">
	import { page } from '$app/state';

	const links = [
		{ href: '/about-us', label: 'About Us' },
		{ href: '/services', label: 'Services' },
		{ href: '/faqs', label: 'FAQs' },
		{ href: '/rates', label: 'Rates' },
		{ href: '/contact-us', label: 'Contact Us' }
	];

	let isOpen = $state(false);

	const isActive = (href: string) => page.url.pathname.startsWith(href);
</script>

<svelte:window onresize={() => (isOpen = false)} />

<header class="relative z-50 border-b border-stone-200 bg-white/90">
	<nav
		class="container relative mx-auto flex items-center justify-between gap-4 px-4 py-5 sm:px-8"
		aria-label="Main navigation"
	>
		<a href="/" class="text-xl font-semibold tracking-tight text-stone-900">Ruffing It Acres</a>

		<button
			type="button"
			class="rounded-md border border-stone-300 px-3 py-2 text-sm font-medium text-stone-700 hover:text-stone-950 md:hidden"
			aria-controls="main-navigation"
			aria-expanded={isOpen}
			onclick={() => (isOpen = !isOpen)}
		>
			{isOpen ? 'Close' : 'Menu'}
		</button>

		<ul
			id="main-navigation"
			class={`${isOpen ? 'flex' : 'hidden'} absolute top-full right-0 left-0 flex-col gap-3 rounded-b-2xl border border-stone-200 bg-white p-5 text-sm font-medium text-stone-700 shadow-xl md:static md:flex md:flex-row md:flex-wrap md:items-center md:justify-end md:gap-x-5 md:gap-y-2 md:border-0 md:bg-transparent md:p-0 md:shadow-none`}
		>
			{#each links as link (link.href)}
				<li class="md:w-auto">
					<a
						href={link.href}
						class={`block w-full rounded-md py-3 text-center md:w-auto md:py-0 md:text-left ${
							isActive(link.href)
								? 'text-stone-950 underline decoration-2 underline-offset-4 md:underline-offset-8'
								: 'hover:text-stone-950'
						}`}
						aria-current={isActive(link.href) ? 'page' : undefined}
						onclick={() => (isOpen = false)}
					>
						{link.label}
					</a>
				</li>
			{/each}
		</ul>
	</nav>
</header>
