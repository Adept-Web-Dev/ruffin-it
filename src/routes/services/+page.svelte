<script lang="ts">
	import { HeroBlock, ProseBlock, TextImageBlock } from '$lib';
	import exitBathImage from '$lib/assets/images/dirty-dog-beagle-running-fast-and-jumping-with-ton-2026-03-09-08-57-43-utc.jpg?enhanced';
	import heroImage from '$lib/assets/images/dogs-running-and-jumping-in-field-on-sunny-day-2026-01-08-06-42-53-utc.jpg?enhanced';
	import overnightImage from '$lib/assets/images/australian-shepherd-dog-and-pitbul-dog-in-a-park-l-2026-03-13-04-21-45-utc.jpg?enhanced';
	import playYardImage from '$lib/assets/images/energetic-dogs-running-in-green-meadow-together-2026-01-09-00-59-53-utc.jpg?enhanced';
</script>

<svelte:head>
	<title>Services | Ruffing It Acres</title>
	<meta name="description" content="Explore Ruffing It Acres services." />
</svelte:head>

<HeroBlock title="Services" imageSrc={heroImage} imageAlt="Dogs running and jumping in a field" />

<TextImageBlock imageSrc={overnightImage} imageAlt="Two dogs playing in a park">
	<h2>Overnight Boarding</h2>

	<p>
		Your dog’s second favorite place to be besides their own warm bed, is ours! Boarding dogs make
		themselves at home in our private rooms, each furnished with their own raised bed or blanket!
	</p>
	<p>
		Our stress-free environment makes it a natural fit for your dog’s individual pace. Our spacious
		outdoor yard is perfect for long days of playing or soaking in the sun and our indoor space is
		created with an “at home” feel, perfect for relaxing to the sound of music or TV.
	</p>
	<p>
		To keep our guests happy we embrace daily rest periods between play sessions. These essential
		naps help maintain a well-balanced, energized dog, ensuring they get both the restorative
		downtime and the action-packed fun they crave.
	</p>
</TextImageBlock>

<TextImageBlock
	imagePosition="left"
	imageSrc={playYardImage}
	imageAlt="Energetic dogs running through a green meadow"
>
	<h2>What’s included with their stay</h2>

	<p>With owners on site, your dog’s personalized needs will not go unmet.</p>
	<ul>
		<li>Climate controlled private room</li>
		<li>Comfortable Raised Dog Bed</li>
		<li>Steady Routine</li>
		<li>Multiple Outside Play Times Each Day</li>
		<li>Food given according to your directions</li>
		<li>Oral Medication Administration as Needed</li>
		<li>Scheduled down times for optimal rest and recovery</li>
	</ul>
</TextImageBlock>

<TextImageBlock imageSrc={exitBathImage} imageAlt="Dirty beagle running and jumping outside">
	<h2>Exit Baths</h2>

	<p>
		While with us, your dog has the opportunity to experience farm life, every dirty inch of it! We
		know that loading a dirty dog into your car is not everyone’s cup of tea. Let us do the hard
		work for you and book your dog an exit bath! (Additional Fee)
	</p>
	<p>Turfed yards are also available for dogs who prefer to keep their paws clean!</p>
</TextImageBlock>

<ProseBlock>
	<h2>Daycare</h2>

	<p>
		Daycare is available on a case by case basis. Give us a call to see if it’s right for your dog!
	</p>
</ProseBlock>
