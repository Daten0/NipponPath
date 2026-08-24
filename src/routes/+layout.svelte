<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Main/Navbar.svelte';
	import Footer from '$lib/components/Main/Footer.svelte';
	import SmokeCursor from '$lib/components/Main/SmokeCursor.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>LPK Artha Karier</title>
	<meta
		name="description"
		content="LPK Artha Karier — Mitra Karier Global, Masa Depan Lebih Cerah. Kuliah sambil kerja magang di Jepang: Program Engineering & Tokutei Ginou, pendaftaran dibuka setiap hari."
	/>
</svelte:head>
<Navbar />
{@render children()}
<Footer />
<!-- <SmokeCursor /> -->
