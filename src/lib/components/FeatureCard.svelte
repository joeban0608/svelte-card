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

<div
	class="mt-10 flex flex-col rounded-xl bg-gradient-to-r from-pink-500 to-purple-500 p-1 shadow-lg"
>
	<div
		class={`${color} relative flex aspect-[3/2] w-full flex-col items-center justify-center gap-4 rounded-lg rounded-b-none p-4`}
	>
		<div
			class="absolute inset-0 animate-pulse rounded-lg rounded-b-none border-2 border-pink-500"
		></div>
		<span class="text-4xl">{icon}</span>
		<span class="digital-font text-sm text-white">{title}</span>
	</div>
	<div class="relative rounded-lg rounded-t-none bg-gray-900 p-6">
		<div
			class="absolute inset-0 animate-pulse rounded-lg rounded-t-none border-2 border-pink-500"
		></div>
		<h2 class="relative text-xl font-semibold text-white">{title}</h2>
		<p class="relative mt-2 text-gray-400">{subtitle}</p>
	</div>
</div>

<style>
	.digital-font {
		font-family: 'Press Start 2P', cursive;
	}
</style>
