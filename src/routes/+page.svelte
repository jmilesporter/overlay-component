<script>
	import { isOverlayOpen } from '../stores/OverlayStore.js';
</script>

<div class="grid place-items-center bg-blue-500 h-screen ">
	<button
		class="bg-red-500  p-4 rounded-xl text-gray-200 hover:-translate-y-1 hover:scale-110  transition ease-in-out duration-300 delay-100 "
		on:click={() => {
			isOverlayOpen.set(true);
			// setTimeout(() => {
			// 	isOverlayOpen.set(false);
			// }, 3000);
		}}>open</button
	>
</div>
