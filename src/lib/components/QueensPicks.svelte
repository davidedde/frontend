<script lang="ts">
	const products = [
		{
			category: 'Serum',
			name: 'Majesty Glow Elixir',
			price: '$124.00',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuBNoNswp5NRMiqDtwxoPtJLBxPEknbsxREx502LuCWvRNm1h1-zUHA0xSI4Q0AvpFuTnQMxWzHmL7W7fD0VxO66Ir3tKUsUqC4g46pzpJJTFi5rTPlbSbBNqdTqi34mIWQlAFxAapRnkrHPBexdb7ygmZp87I-WERQ_xpvCrE7YOOdhUKjn2cSt7WpyFayIYEjCHjIQkPHtShHovlp3dW3aHXHhZpZ1cDKXhBBmmkNXQ9tFKy-6OAdGQy4JDC1h6BX6Fw6R2p01JsY',
			alt: 'A premium face serum in a dark emerald green glass bottle with a gold dropper'
		},
		{
			category: 'Moisturizer',
			name: 'Velvet Court Cream',
			price: '$98.00',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuC53-XgRbI2UDZ8bDOkxxHT-UJd7mI2BVkPqXN4NjQRdSpy5NywF1-JtFahDt1DBrhdLwg89ShLiMAYnwYj-Zbsp0obKvSFbAnX44QNM9CoMNyb1i-AUZqCDeN4IluDcUQ6JUI0uySMBfgImSAhvuUJzsHnv-33XRMySz-9TJS1m5zr69zE-EUp4JXQu4LMj8_tCtnEFS_J7Sjbkp8NfnvUMhvux3EIDApT7732Kobg98Cvw7Fz5HoriarLRlBOaUuta2hP6mVGtbE',
			alt: 'A luxurious rich cream in a matte white porcelain jar with a minimal champagne gold label'
		},
		{
			category: 'Makeup',
			name: 'Sovereign Line Definer',
			price: '$42.00',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuCAtJ9-zADvfqRtNCku93CY-9ltpUtJYULT1K4J8G-dx_smMZ4D5sslaR1oJtm66HSlllhJ1lqjdSf5jgHidIJZh6PRoCMDJOrEStAGpiAveNuW1FMZY99omTgAezuhE8TNt5nVNPXXVvuHpJ85Vgl4fGXTCY3k8lqoRfeEoYwMhM9X7NHhqlnjYnO-657jJO9hdDkIHJJUK4PWZnzoy_hpoTgZPdinPYesbUV3vdB-Gpd8WcvAgClXAwsezirACyGBfPsItvRbdTE',
			alt: 'A sleek black eyeliner pen with a fine gold tip'
		},
		{
			category: 'Tools',
			name: 'The Royal Brush Set',
			price: '$165.00',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuAPLqQATn0UUtnKU-030M-c5Pajp90nWeu8Olrp1BAtTeLSSgd9n0g92MzQmg1cJk28O019DWOBvy04iyqKnoilkV-W4bDXHAatFEq8TuVd-sHkr8p73N6dCCG0VgZ9f6McwK2ugKNNqKj6Z4-M9cBGsYpSkoaEeRg6V933EI0rfx-KOfKNXiu3mhrfF5RzhTa0OUe8fokkV6c2puYQLyMF-5hGmOf6yh8r6Fi5LcpE3WTTzkxiDWgezr1mmRjwilZHNs4k9vdTBZg',
			alt: 'A curated set of three gold-plated makeup brushes held in a minimalist stone canister'
		},
		{
			category: 'Ritual',
			name: 'Gold Standard Polish',
			price: '$85.00',
			image:
				'https://lh3.googleusercontent.com/aida-public/AB6AXuBZM8g5wldOIfyCOqRN03Idg2-g35Ffl_qz2FnwURUKmesuZt8swwkzjTCBCN16QEcVvTlca2bky1Kx0bLotLEyigule9K9y1pxnMYziWFH82nvaqaWtW2gc5PogpT7701Oy1msqgNcpi2GlhGyZv7wW6zVtyLBmja5AfAcMc79z8MYuR5jJtizHuzM5HVXbs9WBlyLWtxO25vt4TMqiT1oMjjSuonDt4VnKoYKN7ehoQXbs5UgEoZPk8hixxAtBoTtz6Lkhkoalxc',
			alt: 'A rich exfoliating facial mask in a dark glass jar'
		}
	];

	let carousel: HTMLDivElement | undefined = $state(undefined);
	let isDown = $state(false);
	let startX = $state(0);
	let scrollLeft = $state(0);

	function handleMouseDown(e: MouseEvent) {
		if (!carousel) return;
		isDown = true;
		startX = e.pageX - carousel.offsetLeft;
		scrollLeft = carousel.scrollLeft;
	}

	function handleMouseLeave() {
		isDown = false;
	}

	function handleMouseUp() {
		isDown = false;
	}

	function handleMouseMove(e: MouseEvent) {
		if (!isDown || !carousel) return;
		e.preventDefault();
		const x = e.pageX - carousel.offsetLeft;
		const walk = (x - startX) * 2;
		carousel.scrollLeft = scrollLeft - walk;
	}
</script>

<section class="bg-surface-container-low py-20">
	<div class="mx-auto mb-12 max-w-[1280px] px-5 md:px-16">
		<h2 class="font-headline text-3xl font-semibold leading-[1.3] text-primary">Queen's Picks</h2>
		<p class="font-body text-base leading-[1.6] text-on-surface-variant">
			The foundational elements of the regal routine.
		</p>
	</div>
	<div
		class="flex gap-6 overflow-x-auto px-5 md:px-16 [&::-webkit-scrollbar]:hidden [-ms-overflow-style:none] [scrollbar-width:none]"
		bind:this={carousel}
		onmousedown={handleMouseDown}
		onmouseleave={handleMouseLeave}
		onmouseup={handleMouseUp}
		onmousemove={handleMouseMove}
		role="list"
	>
		{#each products as product}
			<div class="group w-72 flex-none" role="listitem">
				<div
					class="relative mb-4 aspect-[4/5] overflow-hidden border border-[rgba(212,175,55,0.3)]"
				>
					<img
						class="h-full w-full object-cover transition-opacity duration-300 group-hover:opacity-90"
						src={product.image}
						alt={product.alt}
					/>
					<button
						class="absolute bottom-4 left-1/2 w-4/5 -translate-x-1/2 bg-white py-3 font-button text-sm font-semibold uppercase tracking-[0.05em] text-primary opacity-0 transition-all duration-300 hover:bg-primary hover:text-white group-hover:opacity-100"
					>
						Quick Add
					</button>
				</div>
				<p
					class="mb-1 font-label text-xs font-semibold uppercase tracking-[0.1em] text-secondary"
				>
					{product.category}
				</p>
				<h3 class="mb-2 font-headline text-2xl font-semibold leading-tight text-primary">
					{product.name}
				</h3>
				<p class="font-body text-base leading-[1.6] text-on-surface-variant">{product.price}</p>
			</div>
		{/each}
	</div>
</section>
