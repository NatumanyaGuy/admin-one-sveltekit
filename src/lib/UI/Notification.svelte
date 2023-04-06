<script>
	//Pass color as Prop
	export let _color = 'blue'; //blue, green, red
</script>

<div class="notification {_color}">
	<div class="flex flex-col md:flex-row items-center justify-between space-y-3 md:space-y-0">
		<div>
			<span class="icon"><i class="mdi mdi-buffer" /></span>
			<b>Responsive table</b>
		</div>
		<button type="button" class="button small textual --jb-notification-dismiss">Dismiss</button>
	</div>
</div>
