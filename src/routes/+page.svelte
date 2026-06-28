<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Categories from '$lib/components/Categories.svelte';
	import QueensPicks from '$lib/components/QueensPicks.svelte';
	import Newsletter from '$lib/components/Newsletter.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
	<title>Queenly | Home</title>
	<meta
		name="description"
		content="QUEENLY - Ascend Your Routine. Luxury skincare, makeup, fragrance and tools."
	/>
	<link
		href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&display=swap"
		rel="stylesheet"
	/>
	<link
		href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Playfair+Display:wght@600;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="overflow-x-hidden bg-background text-on-surface selection:bg-primary-container selection:text-on-primary-container">
	<Navbar />
	<main>
		<Hero />
		<Categories />
		<QueensPicks />
		<Newsletter />
	</main>
	<Footer />
</div>
