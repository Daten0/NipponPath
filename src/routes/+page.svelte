<script lang="ts">
	import Hero from '$lib/components/Main/Hero.svelte';
	import EducationSection from '$lib/components/Main/EducationSection.svelte';
	import PlacementSection from '$lib/components/Main/PlacementSection.svelte';
</script>

<main>
	<Hero />
	<EducationSection />
	<PlacementSection />

	<!-- Simple CTA Section Before Footer -->
	<section
		class="relative overflow-hidden bg-linear-to-b from-highlight-light to-highlight py-16 text-center text-primary"
	>
		<div class="brush-texture absolute inset-0" aria-hidden="true"></div>
		<div class="relative container mx-auto px-6">
			<h2 class="mb-4 text-3xl font-bold">Wujudkan Karier Globalmu Bersama LPK Artha Karier!</h2>
			<p class="mb-8 text-primary/80">
				Gaji 10–15 JT sebulan* — kami siap membantu meraih masa depanmu di Jepang! *Sesuai posisi
				dan perusahaan.
			</p>
			<a
				href="https://wa.me/6287822462237"
				target="_blank"
				class="inline-block rounded-full bg-linear-to-b from-primary to-primary-dark px-8 py-3 font-bold text-highlight-light transition hover:from-primary-light hover:to-primary"
			>
				Daftar via WhatsApp
			</a>
		</div>
	</section>
</main>

<style>
	.brush-texture {
		background-image: url('../lib/assets/brush-texture.svg');
		background-repeat: repeat;
		background-size: 800px 400px;
	}
</style>
