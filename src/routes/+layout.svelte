<script>
	// @ts-nocheck
	import '../app.css';
	import NavBar from '$lib/NavBar.svelte';
	import SideNav from '$lib/SideNav.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://cdn.materialdesignicons.com/4.9.95/css/materialdesignicons.min.css"
	/>
	<title>Admin One</title>
</svelte:head>

<SideNav />
<NavBar />
<div class="p-5">
	<slot />
</div>
<Footer />
