<script lang="ts">
	import { twMerge } from 'tailwind-merge';

	interface Props {
		class?: string;
	}

	let { class: className = '' }: Props = $props();
</script>

<h1 class={twMerge(className, 'text-5xl')}>Mastering responsive HTML images 🌉</h1>
