<script lang="ts">
	const conciergeLinks = [
		{ label: 'Shipping & Returns', href: '/' },
		{ label: 'Contact Us', href: '/' },
		{ label: 'FAQs', href: '/' },
		{ label: 'Track Order', href: '/' }
	];

	const discoveryLinks = [
		{ label: 'Ritual Guide', href: '/' },
		{ label: 'Store Locator', href: '/' },
		{ label: 'Ingredients Glossary', href: '/' },
		{ label: 'The Royal Blog', href: '/' }
	];

	const legalLinks = [
		{ label: 'Privacy Policy', href: '/' },
		{ label: 'Terms of Service', href: '/' },
		{ label: 'Accessibility', href: '/' }
	];
</script>

<footer class="w-full border-t border-outline-variant/30 bg-surface-container-low">
	<div class="mx-auto grid max-w-[1280px] grid-cols-1 gap-12 px-5 py-20 md:grid-cols-4 md:px-16">
		<div class="col-span-1">
			<h3 class="mb-4 font-headline text-3xl font-semibold text-primary">QUEENLY</h3>
			<p class="font-body text-base leading-[1.6] text-on-surface-variant">
				Elevating the daily ritual through modern science and ancestral luxury.
			</p>
		</div>
		<div>
			<h4 class="mb-6 font-label text-xs font-semibold uppercase tracking-[0.1em] text-primary">
				Concierge
			</h4>
			<ul class="flex flex-col gap-4">
				{#each conciergeLinks as link}
					<li>
						<a
							class="font-body text-base leading-[1.6] text-on-surface-variant transition-colors hover:text-secondary"
							href={link.href}>{link.label}</a
						>
					</li>
				{/each}
			</ul>
		</div>
		<div>
			<h4 class="mb-6 font-label text-xs font-semibold uppercase tracking-[0.1em] text-primary">
				Discovery
			</h4>
			<ul class="flex flex-col gap-4">
				{#each discoveryLinks as link}
					<li>
						<a
							class="font-body text-base leading-[1.6] text-on-surface-variant transition-colors hover:text-secondary"
							href={link.href}>{link.label}</a
						>
					</li>
				{/each}
			</ul>
		</div>
		<div>
			<h4 class="mb-6 font-label text-xs font-semibold uppercase tracking-[0.1em] text-primary">
				Legals
			</h4>
			<ul class="flex flex-col gap-4">
				{#each legalLinks as link}
					<li>
						<a
							class="font-body text-base leading-[1.6] text-on-surface-variant transition-colors hover:text-secondary"
							href={link.href}>{link.label}</a
						>
					</li>
				{/each}
			</ul>
		</div>
	</div>
	<div class="border-t border-outline-variant/10 px-5 py-8 text-center md:px-16">
		<p
			class="font-label text-xs font-semibold uppercase tracking-widest text-on-surface-variant/60"
		>
			&copy; 2024 QUEENLY BEAUTY. ASCEND YOUR ROUTINE.
		</p>
	</div>
</footer>
