<script lang="ts">
	interface Props {
		color?: string;
		icon?: string;
		title?: string;
		subtitle?: string;
	}
	let {
		color = 'bg-pink-600',
		icon = '📁',
		title = 'Card Title',
		subtitle = 'Short description here.'
	}: Props = $props();
</script>

{#snippet neonGlowDiv(roundedNon: 'top' | 'bottom' | 'all' = 'all')}
	{#if roundedNon === 'top'}
		<div class="absolute inset-0 animate-pulse rounded-t-lg border-2 border-pink-500"></div>
	{:else if roundedNon === 'bottom'}
		<div class="absolute inset-0 animate-pulse rounded-b-lg border-2 border-pink-500"></div>
	{:else}
		<div class="absolute inset-0 animate-pulse rounded-lg border-2 border-pink-500"></div>
	{/if}
{/snippet}

<div
	class="mt-10 flex flex-col rounded-xl bg-gradient-to-r from-pink-500 to-purple-500 p-1 shadow-lg"
>
	<div
		class={`${color} relative flex aspect-[3/2] w-full flex-col items-center justify-center gap-4 rounded-t-lg p-4`}
	>
		{@render neonGlowDiv('top')}
		<span class="text-4xl">{icon}</span>
		<span class="digital-font text-sm text-white">{title}</span>
	</div>
	<div class="ne relative rounded-b-lg bg-gray-900 p-6">
		{@render neonGlowDiv('bottom')}
		<h2 class="relative text-xl font-semibold text-white">{title}</h2>
		<p class="relative mt-2 text-gray-400">{subtitle}</p>
	</div>
</div>

<style>
	.digital-font {
		font-family: 'Press Start 2P', cursive;
	}
</style>
