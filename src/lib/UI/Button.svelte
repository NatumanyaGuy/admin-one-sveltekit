<script>
	import { createEventDispatcher } from 'svelte';
	export let type = 'green';
</script>

<button class="button {type}"> <slot /> </button>
