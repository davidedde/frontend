<script lang="ts">
	let scrolled = $state(false);

	function handleScroll() {
		scrolled = window.scrollY > 20;
	}
</script>

<svelte:window onscroll={handleScroll} />

<nav
	class="sticky top-0 z-50 h-20 border-b border-outline-variant/30 bg-surface/90 backdrop-blur-xl"
	class:shadow-sm={scrolled}
>
	<div class="mx-auto flex h-full w-full max-w-[1280px] items-center justify-between px-5 md:px-16">
		<!-- Left: Navigation Links -->
		<div class="hidden items-center gap-8 md:flex">
			<a
				class="relative font-label text-xs font-semibold uppercase tracking-[0.1em] text-on-surface-variant transition-all duration-300 hover:text-primary after:absolute after:bottom-[-2px] after:left-1/2 after:h-px after:w-0 after:bg-current after:transition-all after:duration-300 after:-translate-x-1/2 hover:after:w-full"
				href="/"
			>
				Shop
			</a>
			<a
				class="relative font-label text-xs font-semibold uppercase tracking-[0.1em] text-on-surface-variant transition-all duration-300 hover:text-primary after:absolute after:bottom-[-2px] after:left-1/2 after:h-px after:w-0 after:bg-current after:transition-all after:duration-300 after:-translate-x-1/2 hover:after:w-full"
				href="/"
			>
				Rituals
			</a>
			<a
				class="relative font-label text-xs font-semibold uppercase tracking-[0.1em] text-on-surface-variant transition-all duration-300 hover:text-primary after:absolute after:bottom-[-2px] after:left-1/2 after:h-px after:w-0 after:bg-current after:transition-all after:duration-300 after:-translate-x-1/2 hover:after:w-full"
				href="/"
			>
				About
			</a>
		</div>

		<!-- Center: Logo -->
		<div class="flex items-center justify-center">
			<span class="font-headline text-2xl font-bold tracking-tight text-primary">QUEENLY</span>
		</div>

		<!-- Right: Actions -->
		<div class="flex items-center gap-6">
			<button
				class="text-on-surface-variant transition-all duration-300 hover:opacity-70 active:scale-95"
			>
				<span class="material-symbols-outlined">person</span>
			</button>
			<button
				class="relative text-on-surface-variant transition-all duration-300 hover:opacity-70 active:scale-95"
			>
				<span class="material-symbols-outlined">shopping_bag</span>
				<span
					class="absolute -top-1 -right-1 rounded-full bg-secondary px-1 text-[8px] text-on-secondary"
				>
					2
				</span>
			</button>
		</div>
	</div>
</nav>
