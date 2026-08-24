<script lang="ts">
	import { MapPin, Phone, AtSign } from 'lucide-svelte';
</script>

<footer id="kontak" class="bg-linear-to-b from-primary to-primary-dark pt-16 pb-8 text-white">
	<div class="container mx-auto px-6">
		<div class="mb-12 grid gap-12 md:grid-cols-3">
			<!-- Brand -->
			<div>
				<h3 class="mb-4 text-2xl font-bold">
					LPK Artha
					<span
						class="bg-linear-to-r from-highlight-light to-highlight bg-clip-text text-transparent"
					>
						Karier
					</span>
				</h3>
				<p class="leading-relaxed text-gray-300">
					Mitra Karier Global, Masa Depan Lebih Cerah. Jalur resmi, aman, dan profesional untuk
					program magang & Tokutei Ginou ke Jepang.
				</p>
			</div>

			<!-- Kontak -->
			<div>
				<h4 class="mb-4 inline-block border-b border-gray-600 pb-2 text-lg font-bold">
					Hubungi Kami
				</h4>
				<ul class="space-y-3">
					<li class="flex items-start gap-3">
						<MapPin size={20} class="mt-1 text-highlight" />
						<span class="text-gray-300">
							Komp. UNHAS ANTANG, Jl. Perdata Raya Blok E No. 2, Kota Makassar, Sulawesi Selatan
						</span>
					</li>
					<li class="flex items-center gap-3">
						<Phone size={20} class="text-highlight" />
						<span class="text-gray-300">087822462237 (WhatsApp)</span>
					</li>
					<li class="flex items-center gap-3">
						<AtSign size={20} class="text-highlight" />
						<span class="text-gray-300">lpk_artha_karier</span>
					</li>
				</ul>
			</div>

			<!-- Links -->
			<div>
				<h4 class="mb-4 inline-block border-b border-gray-600 pb-2 text-lg font-bold">Tautan</h4>
				<ul class="space-y-2">
					<li>
						<a href="#pendidikan" class="text-gray-300 transition hover:text-white"
							>Program Pendidikan</a
						>
					</li>
					<li>
						<a href="#penempatan" class="text-gray-300 transition hover:text-white"
							>Proses Penempatan</a
						>
					</li>
				</ul>
			</div>
		</div>

		<div class="border-t border-gray-700 pt-8 text-center text-sm text-gray-400">
			&copy; {new Date().getFullYear()} LPK Artha Karier. All rights reserved.
		</div>
	</div>
</footer>
