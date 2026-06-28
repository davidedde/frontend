<script lang="ts">
	import { onMount } from 'svelte';

	let visible = $state(false);

	onMount(() => {
		visible = true;
	});
</script>

<section class="relative flex h-screen w-full items-center justify-center overflow-hidden">
	<div class="absolute inset-0 z-0">
		<div
			class="h-full w-full scale-105 bg-cover bg-center transition-transform duration-[10000ms] ease-linear hover:scale-100"
			style="background-image: url('https://lh3.googleusercontent.com/aida-public/AB6AXuD15YtAk96_1qcLqbGUTXuAt3o34zTyqMk6fALMtFQludFFD1unAOKIqkHAKfJAf5rW7WUb1Lk2P7_iBY0yyRHoBlvlbaCEwexEIL7anI6aVixEv4bs6hLkdg9xYbNxikwlr_MBfR2PEdeOhV2hDVxl8ViAIibofgEqaOPVGtHXLeeNb9-PYsx_4v11_HBQWRQlQYLK_ow8Z6ItALmBxnG9oF-Mfd3Nm8PYOLSh43eK1N3FyVrt9VUXIFZUAvKueuac2eOKBkJRX7k')"
		></div>
		<div class="absolute inset-0 bg-primary/10"></div>
	</div>
	<div
		class="relative z-10 px-5 text-center transition-all duration-800"
		class:opacity-0={!visible}
		class:translate-y-5={!visible}
		class:opacity-100={visible}
		class:translate-y-0={visible}
	>
		<h1
			class="mb-6 font-display text-4xl font-bold leading-[1.2] tracking-tighter text-white md:text-5xl md:leading-[1.1]"
		>
			Ascend Your Routine.
		</h1>
		<a
			class="inline-block bg-primary px-12 py-5 font-button text-sm font-semibold uppercase tracking-widest text-white shadow-[0px_4px_20px_rgba(4,57,39,0.05)] transition-colors duration-500 hover:bg-primary-container"
			href="/"
		>
			Shop Skincare
		</a>
	</div>
</section>
