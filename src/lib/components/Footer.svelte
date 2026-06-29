<script lang="ts">
	import BlockWrapper from './BlockWrapper.svelte';

	const year = new Date().getFullYear();
</script>

<BlockWrapper as="footer" class="border-t border-stone-200 bg-white/90 py-6">
	<div
		class="flex flex-col gap-4 text-sm text-stone-600 sm:flex-row sm:items-center sm:justify-between"
	>
		<div>
			<p class="font-semibold text-stone-900">Ruffing It Acres</p>
			<p>47560 SD Hwy 50, Elk Point, SD 57025</p>
		</div>

		<div class="space-y-1 sm:text-right">
			<p>&copy; {year} Ruffing It Acres. All rights reserved.</p>
			<a href="mailto:ruffingitacres@gmail.com" class="hover:text-stone-900">
				ruffingitacres@gmail.com
			</a>
		</div>
	</div>
</BlockWrapper>
