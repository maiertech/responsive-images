<script lang="ts">
	import { Transition } from '@animotion/core';
	import src from '$lib/erasmus-bridge.jpg';

	let ratio: '16/9' | '1/1' | '9/16' | undefined = $state();
</script>

{#if ratio === undefined}
	<img
		{src}
		alt="Erasmus Bridge"
		class="aspect-[16/9] w-[500px] rounded-lg object-cover"
		style="image-rendering: pixelated; filter: contrast(150%) saturate(50%) blur(0.5px) brightness(80%);"
	/>
{/if}

{#if ratio === '16/9'}
	<Transition visible>
		<img {src} alt="Erasmus Bridge" class="aspect-[16/9] w-[500px] rounded-lg object-cover" />
	</Transition>
{/if}

{#if ratio === '1/1'}
	<Transition visible>
		<img {src} alt="Erasmus Bridge" class="aspect-[1/1] w-[500px] rounded-lg object-cover" />
	</Transition>
{/if}

{#if ratio === '9/16'}
	<Transition visible>
		<img {src} alt="Erasmus Bridge" class="aspect-[9/16] w-[300px] rounded-lg object-cover" />
	</Transition>
{/if}

<Transition do={() => (ratio = '16/9')} />
<Transition do={() => (ratio = '1/1')} />
<Transition do={() => (ratio = '9/16')} />
