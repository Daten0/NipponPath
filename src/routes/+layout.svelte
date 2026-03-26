<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Main/Navbar.svelte';
	import Footer from '$lib/components/Main/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Nippon Pathway - Kerja & Pelatihan ke Jepang</title>
  <meta name="description" content="Jasa pelatihan dan penempatan tenaga kerja ke Jepang terpercaya." />
</svelte:head>
<Navbar />
{@render children()}
<Footer />