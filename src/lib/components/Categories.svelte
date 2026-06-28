<script lang="ts">
	const categories = [
		{
			name: 'Skincare',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuCsxNVInTYgosbRXsGBZhsfqtPYx1lpGZmtG7GWOlrdIVdgOMFpzwO7m3ktjdexSio5o0Kbt1DEVA4MOip9642uSGPAFh26gyItcWF2YmKZ0SlYVVe5Bdq1jdlUViL_CsOYhUGW6rko1mpJqu1ZXThPFroZSMJo6LGKVziteiwieyA3uItU2l-yI2NjGnbBKhj_3hNs5xwOLAEXr1HE8TrwLdW5ig7uZQKlYk3qYIL378Hy8LRXoygmWEPZOncZ4CBz7Q8rOcVZ8n4',
			alt: 'A serene close-up of a high-end amber glass skincare bottle on a marble surface'
		},
		{
			name: 'Makeup',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuCCU8KFZx8hwGsiX4JbWy-_WmWQr4x-e1oQtCbQdkrcKAQGqWCymIaLsynS5IEd_z_4GMOQxH4E_iuNP5va87B9TSTKKLT6FmXqGwbHUQOEsiBcPEhD_CSw5JAzRJpPPxne_Pi8LcDmSHKnEPJ8y-j27NcZYOm7yotFZdOQBnZ-6JObAGrD5m__eXMUQtQVGjnh7lPKc591WzDjXBTXddsAqYTHpyOtEY_sRc_rpQnRphjMDffa1biUhSvBq1xD_8qHqPKa6vFe9V0',
			alt: 'Exquisite makeup palette with shimmering earthy tones and a elegant gold case'
		},
		{
			name: 'Fragrance',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuBzpvTs1Yt-pCD3-ZKmkFuDGSBjkDlWKTfN7ZpHpZvnnwhYbNIWoukLIQs7UCZMW3Ft-9E80vrYz28PJFp4KZDpb9Ac7x7vidfrAaxauC8xQJH2bS6OO8GtAWtQ1ZxX8W7cN5Vrx1H-IcPN8wdMXLEzZceRhri81VO2wJMQA7FOx1sbyaJOrjczv7mezCUj5vxwMCYBoNp_RAWWV2o4ag4o4bge7YEvSghpamNJl-ormEnYCZACccYgi_c81ut38qB8cCe7_AwyqyM',
			alt: 'A minimalist perfume bottle crafted from heavy crystal'
		},
		{
			name: 'Tools',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuBoGzHpyEhgzzg3ZIbqEsyKKmcTm8dFVTy9rCHZMSbLsmHvsbzsBi_vxCuV-gOMDv2pokPtAcwxZEDPW-NTZgqeQlskqKURg5bZiTtpNSV4WFUZokRVSEwQnjtM9IYVTHrkkS2UNdZQVddjoF5wf1a8LqftQjf7U68M38ltP6OGmF8eJhEio8qk8tjBQqhaUJOYFOZjl-Ha75-3nE10UJ4-s4p9l-TJaIu6wjWL-IkX67p530ImQTimwliAVTdLGXPKjkjzBg4_1q8',
			alt: 'High-end facial tools including a rose quartz roller and a brass-finished gua sha tool'
		}
	];
</script>

<section class="mx-auto max-w-[1280px] px-5 py-20 md:px-16">
	<div class="mb-12 flex items-end justify-between">
		<div>
			<h2 class="mb-2 font-headline text-3xl font-semibold leading-[1.3] text-primary">
				Curated Collections
			</h2>
			<p class="font-body text-base leading-[1.6] text-on-surface-variant">
				The tools for your daily coronation.
			</p>
		</div>
		<a
			class="hidden border-b border-primary pb-1 font-label text-xs font-semibold uppercase tracking-[0.1em] md:block"
			href="/"
		>
			Explore All
		</a>
	</div>
	<div class="grid grid-cols-1 gap-6 md:grid-cols-4">
		{#each categories as category}
			<a
				class="group relative aspect-[3/4] overflow-hidden border border-[rgba(212,175,55,0.3)]"
				href="/"
			>
				<div
					class="absolute inset-0 bg-cover bg-center transition-transform duration-700 group-hover:scale-110"
					style="background-image: url('{category.image}')"
					role="img"
					aria-label={category.alt}
				></div>
				<div
					class="absolute inset-0 bg-black/5 transition-colors group-hover:bg-black/20"
				></div>
				<div class="absolute bottom-6 left-6">
					<span
						class="font-label text-xs font-semibold uppercase tracking-widest text-white"
					>
						{category.name}
					</span>
				</div>
			</a>
		{/each}
	</div>
</section>
