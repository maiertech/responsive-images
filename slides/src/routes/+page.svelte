<script lang="ts">
	import { Presentation, Slide, Transition } from '@animotion/core';
	import { Overview, Title, Images } from '$lib/components';
</script>

<Presentation options={{ history: true, transition: 'slide', controls: true, progress: true }}>
	<Slide class="h-full place-content-center place-items-center">
		<Images />
	</Slide>

	<Slide class="h-full place-content-center place-items-center">
		<Title class="mb-16" />
		<Overview class="mb-16" />
		<Transition visible>
			<p class="text-2xl">Transform your website with stunning, perfectly optimized images.</p>
		</Transition>
	</Slide>

	<!-- Video 01 -->

	<Slide class="h-full place-content-center place-items-center">
		<Title class="mb-16" />
		<Overview highlight={1} class="mb-16" />
	</Slide>

	<Slide class="h-full place-content-center place-items-center">
		<h1 class="mb-12 text-5xl">What you will learn</h1>

		<ul class="flex flex-col gap-4 text-left text-2xl">
			<li>Intrinsic size and aspect ratio</li>
			<li>Replaced elements</li>
			<li>Layout shift</li>

			<li>Sizing the <code>&lt;img /&gt;</code> element</li>
		</ul>
	</Slide>

	<!-- Video 02 -->

	<Slide class="h-full place-content-center place-items-center">
		<Title class="mb-16" />
		<Overview highlight={2} class="mb-16" />
	</Slide>
</Presentation>
