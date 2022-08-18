<script>
	import '../app.css';
	import { isOverlayOpen } from '../stores/OverlayStore.js';
	import Overlay from '../components/Overlay.svelte';
</script>

{#if $isOverlayOpen}
	<div>
		<Overlay>
			<div>content</div>
		</Overlay>
	</div>
{/if}
<main>
	<slot />
</main>
