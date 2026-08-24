<script lang="ts">
	import { BookOpen, GraduationCap, Backpack } from 'lucide-svelte';

	const programs = [
		{
			icon: BookOpen,
			title: 'Kelas Bahasa Jepang',
			desc: 'Pendidikan bahasa dan persiapan kerja ke Jepang dengan bimbingan menyeluruh.'
		},
		{
			icon: GraduationCap,
			title: 'Pilihan Jurusan',
			desc: 'Teknik Mesin, Teknik Elektro, Informatika, dan Agribisnis Pertanian.'
		},
		{
			icon: Backpack,
			title: 'Fasilitas Lengkap',
			desc: 'Asrama dan fasilitasnya, buku modul lengkap, alat tulis lengkap, serta guru profesional.'
		}
	];
</script>

<section id="pendidikan" class="bg-linear-to-b from-white to-primary-soft py-20">
	<div class="container mx-auto px-6">
		<div class="mb-16 text-center">
			<h2 class="mb-4 text-3xl font-bold text-primary md:text-4xl">
				Kelas Bahasa & Pelatihan Kerja
			</h2>
			<div class="mx-auto h-1 w-20 bg-highlight"></div>
			<p class="mx-auto mt-4 max-w-2xl text-gray-600">
				Pendaftaran dibuka setiap hari. Biaya pendidikan 10 JT — raih pengalaman kerja
				internasional, tingkatkan kompetensi dan masa depan Anda.
			</p>
		</div>

		<div class="grid gap-8 md:grid-cols-3">
			{#each programs as program (program.title)}
				<div
					class="rounded-xl border-t-4 border-highlight bg-linear-to-b from-white to-gray-50 p-8 shadow-lg transition hover:shadow-xl"
				>
					<div
						class="mb-6 flex h-14 w-14 items-center justify-center rounded-full bg-primary-soft text-primary"
					>
						<program.icon size={28} />
					</div>
					<h3 class="mb-3 text-xl font-bold text-gray-800">{program.title}</h3>
					<p class="leading-relaxed text-gray-600">{program.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
