<script lang="ts">
	let email = $state('');

	function handleSubmit(e: Event) {
		e.preventDefault();
		// Newsletter signup logic
		email = '';
	}
</script>

<section class="border-t border-outline-variant/30 py-20">
	<div class="mx-auto max-w-2xl px-5 text-center">
		<h2 class="mb-4 font-headline text-3xl font-semibold uppercase tracking-tighter text-primary">
			Join the Court
		</h2>
		<p class="mb-6 font-body text-base leading-[1.6] text-on-surface-variant">
			Receive exclusive access to ritual launches, royal rewards, and curated beauty insights.
		</p>
		<form class="flex flex-col items-end gap-4 md:flex-row" onsubmit={handleSubmit}>
			<div class="w-full flex-grow">
				<input
					class="w-full border-0 border-b border-outline bg-transparent px-0 py-4 font-label text-xs font-semibold uppercase tracking-[0.1em] placeholder:text-outline/50 focus:border-secondary focus:ring-0"
					placeholder="YOUR EMAIL ADDRESS"
					type="email"
					bind:value={email}
				/>
			</div>
			<button
				class="w-full bg-primary px-10 py-5 font-button text-sm font-semibold uppercase tracking-widest text-white transition-colors duration-300 hover:bg-secondary md:w-auto"
				type="submit"
			>
				Subscribe
			</button>
		</form>
	</div>
</section>
