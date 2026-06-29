<script lang="ts">
	import { HeroBlock, TextImageBlock } from '$lib';
	import boardingImage from '$lib/assets/images/two-happy-dogs-standing-together-in-the-grass-2026-03-09-09-20-43-utc.jpg?enhanced';
	import heroImage from '$lib/assets/images/group-of-cute-playful-dogs-running-in-the-meadow-f-2026-01-07-07-21-43-utc.jpg?enhanced';
	import propertyImage from '$lib/assets/images/dog-sitting-in-the-tall-grass-on-sunny-day-2026-03-19-02-21-00-utc.jpg?enhanced';
</script>

<svelte:head>
	<title>Ruffing It Acres | Home</title>
	<meta
		name="description"
		content="Ruffing It Acres is a family owned and operated dog boarding facility between Elk Point and Vermillion, SD."
	/>
</svelte:head>

<HeroBlock
	title="Welcome to Ruffing It Acres!"
	subtitle="Where It’s Anything But Rough!"
	imageSrc={heroImage}
	imageAlt="Group of dogs playing in a grassy yard"
/>

<TextImageBlock imageSrc={propertyImage} imageAlt="Dog sitting in tall grass on a sunny day">
	<h2>We are your dog’s home away from home!</h2>

	<p>
		Ruffing It Acres is a family owned and operated dog boarding facility located in between Elk
		Point and Vermillion, SD, just 5 minutes from I-29. Built on a scenic 120 acres, our outdoor
		play yards span acres of fun providing an escape for dogs craving fresh air and adventure, while
		our mowed walking paths meander through the farmstead for stimulating daily walks.
	</p>
</TextImageBlock>

<TextImageBlock
	imagePosition="left"
	imageSrc={boardingImage}
	imageAlt="Two happy dogs standing together in the grass"
>
	<h2 class="text-red-600">Comfortable Boarding, Personalized Care</h2>

	<p>
		Inside, our building is set up with comfort in mind: fully climate controlled to beat the summer
		heat, a heated floor for those cold winter days, and a family room for afternoon snuggles,
		family often included!
	</p>
	<p>
		We offer overnight boarding with private rooms, comfortable beds and bedding, and plenty of play
		time! With fewer dogs on site, we deliver truly personalized care and a predictable routine in a
		calmer, safer environment. It’s not just about where your dog spends their day, it’s knowing
		they are in the best hands.
	</p>
</TextImageBlock>
