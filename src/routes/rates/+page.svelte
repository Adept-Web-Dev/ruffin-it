<script lang="ts">
	import { HeroBlock, ProseBlock, RatesBlock } from '$lib';
	import heroImage from '$lib/assets/images/group-of-cute-playful-dogs-running-in-the-meadow-f-2026-03-18-09-33-50-utc.jpg?enhanced';

	const rateCards = [
		{
			title: 'Standard Room',
			price: '$40/night',
			description: '4x6 private room'
		},
		{
			title: 'Family Room',
			price: '$60/night (?)',
			description: '8x6 private room',
			details: ['Additional dogs per kennel: $30 each/night']
		},
		{
			title: 'Whole Home Booking',
			price: '$350/night',
			description: 'Includes 11 4x6 kennels and all indoor/outdoor play yards'
		},
		{
			title: 'Exit Baths',
			price: '$30–50',
			description: 'Bath pricing is for current boarding clients only'
		}
	];
</script>

<svelte:head>
	<title>Boarding Rates | Ruffing It Acres</title>
	<meta name="description" content="View boarding rates for Ruffing It Acres." />
</svelte:head>

<HeroBlock
	title="Boarding Rates"
	imageSrc={heroImage}
	imageAlt="Group of playful dogs running in a meadow"
/>

<RatesBlock cards={rateCards} />

<ProseBlock>
	<ul>
		<li>
			If your dog has never boarded before, please give us a call to schedule a meet and greet. Each
			dog reacts differently to a boarding environment and we would love to ease that transition by
			introducing them to it with you present.
		</li>
		<li><strong>Peak pricing:</strong> Additional $5.00 per night per dog.</li>
		<li>
			<strong>Peak pricing:</strong> Additional $5.00 per night per dog on federal holidays. This is
			to cover the cost of extra staffing. See calendar for list of days.
			<span class="text-red-600">
				Confirm whether this should link to a calendar or include a list of dates, since some
				holiday dates change each year.
			</span>
		</li>
		<li>
			Whole Home Booking is not available for peak days. To book the Whole Home option, please call
			us directly.
		</li>
		<li>
			Our second dog boarding rate applies only if the room is shared. If you request individual
			rooms for your dogs, the first dog boarding rate will apply.
		</li>
	</ul>
</ProseBlock>
