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
	<div class={`${color} relative h-auto w-full rounded-lg rounded-b-none`}>
		<div
			class="absolute inset-0 animate-pulse rounded-lg rounded-b-none border-2 border-pink-500"
		></div>
		<img
			src="https://dummyimage.com/600x400/000/fff&text=joeban"
			alt="1"
			class="rounded-lg opacity-5"
		/>
		<div
			class="absolute top-1/2 left-1/2 flex -translate-x-1/2 -translate-y-1/2 flex-col items-center justify-center gap-4"
		>
			<span class="text-4xl">{icon}</span>
			<span class="digital-font text-sm text-white">{title}</span>
		</div>
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
