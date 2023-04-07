<script>
	import TitleBar from '$lib/Dashboard/TitleBar.svelte';
	import Notification from '$lib/UI/Notification.svelte';
	import Table from '$lib/UI/Table.svelte';
</script>

<TitleBar _page="Tables" />
<Notification color="red" message="This is the Table Page." dismissable={true} />
<Table />
