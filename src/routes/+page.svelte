<script>
	// @ts-nocheck
	import Cards from '$lib/Dashboard/Cards.svelte';
	import HeroBar from '$lib/Dashboard/HeroBar.svelte';
	import TitleBar from '$lib/Dashboard/TitleBar.svelte';
	import Notification from '$lib/UI/Notification.svelte';
	import Table from '$lib/UI/Table.svelte';
</script>

<svelte:head>
	<title />
</svelte:head>

<TitleBar _page="Dashboard" />
<HeroBar />
<section class="section main-section">
	<Cards />
	<Notification color="blue" message="This is the Dashboard" dismissable={true} />
	<Table />
</section>
