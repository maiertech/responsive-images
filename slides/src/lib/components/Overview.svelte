<script lang="ts">
	import { Transition } from '@animotion/core';
	import { twMerge } from 'tailwind-merge';

	interface Props {
		highlight?: number | undefined;
		class?: string;
	}

	const { highlight = undefined, class: className = '' }: Props = $props();
</script>

<div class={twMerge(className, 'grid grid-cols-2 gap-10')}>
	<Transition visible={highlight !== undefined}>
		<ol class="flex list-decimal flex-col gap-4 pl-8 text-left text-2xl">
			<li class={highlight === 1 ? 'font-bold text-orange-300' : ''}>
				Exploring the <code>&lt;img /&gt;</code> element
			</li>
			<li class={highlight === 2 ? 'font-bold text-orange-300' : ''}>
				Rendering images within containers
			</li>
			<li class={highlight === 3 ? 'font-bold text-orange-300' : ''}>
				Optimizing fixed-size images
			</li>
			<li class={highlight === 4 ? 'font-bold text-orange-300' : ''}>
				Responsive images using width descriptors
			</li>
			<li class={highlight === 5 ? 'font-bold text-orange-300' : ''}>
				Using an image API (part 1)
			</li>
		</ol>
	</Transition>
	<Transition visible={highlight !== undefined}>
		<ol class="flex list-decimal flex-col gap-4 pl-8 text-left text-2xl" start="6">
			<li>Next-gen image formats</li>
			<li>Using an image API (part 2)</li>
			<li>Advanced performance tweaks</li>
			<li>Rendering images in different CSS layouts</li>
			<li>Art direction</li>
		</ol>
	</Transition>
</div>
