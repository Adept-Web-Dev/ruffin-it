<script lang="ts">
	import { HeroBlock, TextImageBlock } from '$lib';
	import flowerDogImage from '$lib/assets/images/happy-dog-with-a-flower-in-a-field-2026-01-08-00-35-20-utc.jpg?enhanced';
	import heroImage from '$lib/assets/images/dog-sitting-on-a-sunny-spring-day-in-a-flower-mead-2026-01-06-10-05-56-utc.jpg?enhanced';
	import restingDogsImage from '$lib/assets/images/two-dogs-rest-in-a-meadow-of-wildflowers-2026-03-16-02-12-22-utc.jpg?enhanced';
</script>

<svelte:head>
	<title>About Us | Ruffing It Acres</title>
	<meta
		name="description"
		content="Learn about Ruffing It Acres, a family owned and operated dog boarding facility focused on individualized care."
	/>
</svelte:head>

<HeroBlock
	title="About Ruffing It Acres"
	subtitle="A long-awaited dream built for dogs to feel at home"
	class="prose-headings:text-red-300"
	imageSrc={heroImage}
	imageAlt="Dog sitting in a sunny flower meadow"
/>

<TextImageBlock imageSrc={flowerDogImage} imageAlt="Happy dog with a flower in a field">
	<h2 class="text-red-600">Jacki’s long-awaited dream</h2>

	<p>
		Ruffing It Acres is the long awaited dream of its owner, Jacki. What started as an animal
		obsession in her youth, developed into a career as an Animal Control Officer and a Humane
		Officer has blossomed into creating a space where dogs are excited to go while their owners are
		away.
	</p>
	<p>
		After witnessing the stress that a typical kennel environment can cause on the best of dogs
		first hand, Jacki knew dogs needed a safe and inviting place where their comfort is the most
		important detail.
	</p>
</TextImageBlock>

<TextImageBlock
	imagePosition="left"
	imageSrc={restingDogsImage}
	imageAlt="Two dogs resting in a meadow of wildflowers"
>
	<h2 class="text-red-600">Family care with room to rest and play</h2>

	<p>
		Ruffing It Acres is family owned and operated with individualized care as our focus. With us,
		your dog is more than just a number, they are a member of the family.
	</p>
	<p>
		We offer overnight boarding with a private room for a peaceful rest, comfortable beds and
		bedding and plenty of play time! Your dog will spend their day in a calm, stress-free
		environment with predictable routines where they can rest, play, and feel at home being
		themselves.
	</p>
	<p>
		Because at the end of the day, it’s not just about where your dog spends their day, it’s knowing
		they are in the right hands.
	</p>
</TextImageBlock>
