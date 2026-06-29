<script lang="ts">
	import { AccordionBlock, HeroBlock, ProseBlock } from '$lib';
	import heroImage from '$lib/assets/images/group-of-dogs-on-a-foggy-autumn-morning-dogs-sitt-2026-03-25-02-15-21-utc.jpg?enhanced';

	const faqs = [
		{
			question: 'What should I pack for my dog when boarding?',
			items: [
				'Their regular food from home with written instructions. No need to portion out each meal, though you may if you like — our staff will follow your feeding instructions.',
				'Any oral medications they are on with written instructions on administration.',
				'A secure collar and leash.',
				'Their vaccination records.',
				'Please don’t bring anything of importance to you or your dog. We cannot guarantee that items won’t be lost or damaged.'
			]
		},
		{
			question: 'Are there any breed/size restrictions?',
			answer: [
				'Currently we do not have any restrictions and evaluate each dog individually. For safety and comfort we separate dogs into playgroups based on size and temperament. We do reserve the right to turn away any dogs for safety reasons or if the dog seems distressed in our environment.'
			]
		},
		{
			question: 'Do you provide grooming?',
			answer: ['We do not provide grooming, YET! We have big plans for the future!']
		},
		{
			question: 'What are your business hours?',
			placeholder: 'Placeholder answer needed from client.'
		},
		{
			question: 'What vaccinations does my dog need to visit Ruffing It Acres?',
			answer: ['We require all dogs to be current on Rabies, Distemper/Parvo, and Bordatella.']
		},
		{
			question: 'What if I am late to get my dog?',
			answer: [
				'We understand that life can get crazy and we all run late from time to time. Occasionally late pick-ups can be pre-arranged. If you are unable to pick up your dog by (insert time here) and an after hours pick-up cannot be arranged, your dog will be checked into boarding for the night and charged the nightly rate.'
			]
		},
		{
			question: 'Is Ruffing It Acres open 365 days a year?',
			answer: [
				'Yes and no. We are here 365 days a year to care for your dogs, but we are closed for pick-ups or drop-offs on Fourth of July, Thanksgiving, Christmas and New Years. We also have shortened hours on Christmas Eve and New Year’s Eve.'
			]
		},
		{
			question: 'Can I tour the facility before booking?',
			answer: [
				'Having new people in and out of the facility can stress out dogs easily so tours are available by appointment only and will be scheduled at lower capacity times.'
			]
		},
		{
			question: 'Can my dog visit Ruffing It Acres if they don’t get along with other dogs?',
			answer: [
				'Dogs who prefer people over other dogs are welcome at Ruffing It Acres as long as they are friendly with staff. These dogs will get one-on-one play time with staff along with rest time in their suites. Out-of-suite play might be more limited based on capacity, but they still get plenty of attention and care.'
			]
		},
		{
			question: 'How do I make a reservation?',
			placeholder: 'Placeholder answer needed from client.'
		}
	];
</script>

<svelte:head>
	<title>FAQs | Ruffing It Acres</title>
	<meta
		name="description"
		content="Frequently asked questions about boarding at Ruffing It Acres."
	/>
</svelte:head>

<HeroBlock
	title="Frequently Asked Questions"
	subtitle="Helpful details before your dog’s stay"
	class="prose-headings:text-red-300"
	imageSrc={heroImage}
	imageAlt="Group of dogs sitting together on a foggy morning"
/>

<ProseBlock class="text-red-600 prose-headings:text-red-600">
	<h2>Before Your Dog’s Stay</h2>

	<p>
		Planning your dog’s stay should feel simple and reassuring. Here are answers to some of the
		questions we hear most often about what to bring, how we care for dogs, and what to expect at
		Ruffing It Acres.
	</p>
</ProseBlock>

<AccordionBlock items={faqs} />
