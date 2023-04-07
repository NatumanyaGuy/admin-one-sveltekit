<script>
	import { fade } from 'svelte/transition';
	export let color = 'blue'; //blue, green, red
	export let message = 'Responsive table';
	export let dismissable = true;
	let show = true;
</script>

{#if show}
	<div class="notification {color}">
		<div class="flex flex-col md:flex-row items-center justify-between space-y-3 md:space-y-0">
			<div>
				<span class="icon"><i class="mdi mdi-buffer" /></span>
				<b>{message}</b>
			</div>
			{#if dismissable}
				<button
					type="button"
					class="button small textual --jb-notification-dismiss"
					on:click={() => {
						show = false;
					}}>Dismiss</button
				>
			{/if}
		</div>
	</div>
{/if}
