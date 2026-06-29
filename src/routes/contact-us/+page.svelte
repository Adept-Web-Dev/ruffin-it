<script lang="ts">
	import { ContactBlock, HeroBlock, Image, RichText } from '$lib';
	import heroImage from '$lib/assets/images/group-of-different-breed-dogs-during-a-walk-in-the-2026-03-16-03-30-06-utc.jpg?enhanced';
</script>

<svelte:head>
	<title>Contact Us | Ruffing It Acres</title>
	<meta name="description" content="Contact Ruffing It Acres in Elk Point, South Dakota." />
</svelte:head>

<HeroBlock title="Contact Us" imageSrc={heroImage} imageAlt="Group of dogs walking together" />

<ContactBlock formClass="border-red-600 ring-2 ring-red-600 ring-offset-2">
	{#snippet details()}
		<div class="space-y-8">
			<RichText class="prose-headings:text-red-600">
				<h3>Questions?</h3>
				<p class="text-balance">
					If you have any questions about our services, please don’t hesitate to contact us!
				</p>
			</RichText>

			<RichText class="ml-4 border-l border-stone-800 pl-4">
				<p>
					<span class="text-stone-500">Phone:</span>
					<span>(will get a phone closer to opening)</span>
				</p>
				<p>
					<span class="text-stone-500">Email:</span>
					<a
						href="mailto:ruffingitacres@gmail.com"
						class="text-stone-900 underline underline-offset-4"
					>
						ruffingitacres@gmail.com
					</a>
				</p>
			</RichText>

			<div class="space-y-4">
				<RichText>
					<h3>Where to find us</h3>
				</RichText>

				<RichText>
					<p class="ml-4 border-l border-stone-800 pl-4">
						47560 SD Hwy 50<br />
						Elk Point, SD 57025
					</p>
					<p>
						During the winter months, please check with us before arriving as we have an alternate
						entrance if there is heavy snow.
					</p>
				</RichText>
			</div>
			<Image
				width={800}
				height={450}
				alt="Placeholder for a Google Map snapshot of Ruffing It Acres"
				class="aspect-video rounded-2xl shadow-sm"
			/>
		</div>
	{/snippet}

	{#snippet form()}
		<RichText class="mb-6 text-red-600 prose-headings:text-red-600">
			<h3>Send Us a Message</h3>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipisicing elit. Suscipit aspernatur perspiciatis
				enim autem tenetur corrupti inventore hic error.
			</p>
		</RichText>

		<form class="space-y-5" onsubmit={(event) => event.preventDefault()}>
			<div>
				<label for="name" class="block font-medium text-stone-900">Name</label>
				<input
					id="name"
					name="name"
					type="text"
					autocomplete="name"
					class="mt-2 block w-full rounded-md border-stone-300 shadow-sm focus:border-stone-900 focus:ring-stone-900"
				/>
			</div>

			<div>
				<label for="email" class="block font-medium text-stone-900">Email</label>
				<input
					id="email"
					name="email"
					type="email"
					autocomplete="email"
					class="mt-2 block w-full rounded-md border-stone-300 shadow-sm focus:border-stone-900 focus:ring-stone-900"
				/>
			</div>

			<div>
				<label for="phone" class="block font-medium text-stone-900">Phone</label>
				<input
					id="phone"
					name="phone"
					type="tel"
					autocomplete="tel"
					class="mt-2 block w-full rounded-md border-stone-300 shadow-sm focus:border-stone-900 focus:ring-stone-900"
				/>
			</div>

			<div>
				<label for="message" class="block font-medium text-stone-900">Message</label>
				<textarea
					id="message"
					name="message"
					rows="5"
					class="mt-2 block w-full rounded-md border-stone-300 shadow-sm focus:border-stone-900 focus:ring-stone-900"
				></textarea>
			</div>

			<button
				type="submit"
				class="inline-flex rounded-md bg-stone-900 px-5 py-3 font-semibold text-white hover:bg-stone-700"
			>
				Send Message
			</button>
		</form>
	{/snippet}
</ContactBlock>
