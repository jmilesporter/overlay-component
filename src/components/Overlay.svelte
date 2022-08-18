<script>
	import { isOverlayOpen } from '../stores/OverlayStore.js';
	import { fade } from 'svelte/transition';
</script>

<div
	class="w-screen h-screen fixed top-0 left-0 grid justify-center items-center z-10 bg-blue-200 "
	on:click={() => {
		isOverlayOpen.set(false);
	}}
	transition:fade
>
	<div class="bg-green-500 text-white rounded-xl px-28 py-20 relative " on:click|stopPropagation>
		<button
			class="absolute top-2 right-3 text-xl text-gray-200 hover:-translate-y-0.5 transition-transform"
			on:click={() => {
				isOverlayOpen.set(false);
			}}>&times;</button
		>
		<slot />
	</div>
</div>
