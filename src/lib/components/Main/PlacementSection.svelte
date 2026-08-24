<script lang="ts">
	import { FileText, ClipboardCheck, Plane, Handshake } from 'lucide-svelte';

	const steps = [
		{
			icon: FileText,
			title: 'Daftar & Berkas',
			desc: 'Kartu Keluarga, Akte Kelahiran, KTP, ijazah terakhir, dan passport.'
		},
		{
			icon: ClipboardCheck,
			title: 'Seleksi',
			desc: 'Laki-laki/perempuan, usia 18–30 tahun, lulusan SMA/SMK/Paket C–Sarjana Teknik.'
		},
		{
			icon: Handshake,
			title: 'Pelatihan & Visa',
			desc: 'Kelas bahasa intensif dan pengurusan COE/Visa.'
		},
		{ icon: Plane, title: 'Pemberangkatan', desc: 'Pendampingan hingga tiba di Jepang.' }
	];
</script>

<section id="penempatan" class="bg-linear-to-b from-primary-soft to-white py-20">
	<div class="container mx-auto px-6">
		<div class="mb-16 text-center">
			<h2 class="mb-4 text-3xl font-bold text-primary md:text-4xl">Proses Penempatan</h2>
			<div class="mx-auto h-1 w-20 bg-highlight"></div>
			<p class="mt-4 text-gray-600">
				Jalur resmi, aman, dan profesional — didukung mitra Jepang yang terpercaya.
			</p>
		</div>

		<div class="grid gap-6 md:grid-cols-4">
			{#each steps as step, index (step.title)}
				<div class="relative flex flex-col items-center text-center">
					<!-- Connector Line (Desktop Only) -->
					{#if index < steps.length - 1}
						<div
							class="absolute top-8 left-1/2 -z-10 hidden h-0.5 w-full bg-gray-200 md:block"
						></div>
					{/if}

					<div
						class="z-10 mb-4 flex h-16 w-16 items-center justify-center rounded-full bg-linear-to-br from-primary-light to-primary-dark text-white shadow-lg"
					>
						<step.icon size={24} />
					</div>
					<h3 class="mb-2 text-lg font-bold text-gray-800">{step.title}</h3>
					<p class="text-sm text-gray-500">{step.desc}</p>
				</div>
			{/each}
		</div>

		<!-- Mitra Section -->
		<div class="mt-20 text-center">
			<p class="mb-6 font-medium text-gray-500">DIPERCAYA OLEH PERUSAHAAN JEPANG</p>
			<div
				class="flex flex-wrap justify-center gap-8 opacity-60 grayscale transition duration-500 hover:grayscale-0"
			>
				<!-- Placeholder Logo Mitra -->
				<div class="h-10 w-32 rounded bg-gray-300"></div>
				<div class="h-10 w-32 rounded bg-gray-300"></div>
				<div class="h-10 w-32 rounded bg-gray-300"></div>
				<div class="h-10 w-32 rounded bg-gray-300"></div>
			</div>
		</div>
	</div>
</section>
