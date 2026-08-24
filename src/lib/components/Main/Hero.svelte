<script lang="ts">
	import { ArrowRight } from 'lucide-svelte';
</script>

<section
	class="relative flex h-screen items-center justify-center overflow-hidden bg-linear-to-b from-primary via-primary-light to-primary-dark text-white"
>
	<!-- Overlay Gelap -->
	<div class="absolute inset-0 z-10 bg-black opacity-50"></div>

	<!-- Background Image (Ganti URL dengan gambar asli nanti) -->
	<div
		class="absolute inset-0 z-0 bg-[url('https://images.unsplash.com/photo-1542051841857-5f90071e7989?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80')] bg-cover bg-center"
	></div>

	<div class="relative z-20 container mx-auto px-6 text-center">
		<h1 class="mb-6 text-4xl leading-tight font-bold md:text-6xl">
			Kuliah Sambil <br /> Kerja Magang <span class="text-highlight">di Jepang</span>
		</h1>
		<p class="mx-auto mb-8 max-w-2xl text-lg text-gray-200 md:text-xl">
			Raih Ilmu, Pengalaman Kerja dan Penghasilan Sekaligus! Program Magang Engineering & Tokutei
			Ginou — jalur resmi, aman, dan profesional. Kuota terbatas!
		</p>
		<div class="flex flex-col justify-center gap-4 md:flex-row">
			<a
				href="#kontak"
				class="flex items-center justify-center gap-2 rounded-lg bg-linear-to-b from-highlight-light to-highlight px-8 py-3 font-bold text-primary transition hover:from-highlight hover:to-highlight-dark"
			>
				Daftar Sekarang <ArrowRight size={20} />
			</a>
			<a
				href="#pendidikan"
				class="rounded-lg border-2 border-white bg-transparent px-8 py-3 font-bold text-white transition hover:bg-linear-to-b hover:from-white hover:to-gray-200 hover:text-primary"
			>
				Lihat Program
			</a>
		</div>
	</div>
</section>
