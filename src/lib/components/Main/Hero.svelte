<script lang="ts">
  import { ArrowRight } from 'lucide-svelte';
</script>

<section class="relative bg-blue-900 h-screen flex items-center justify-center text-white overflow-hidden">
  <!-- Overlay Gelap -->
  <div class="absolute inset-0 bg-black opacity-50 z-10"></div>
  
  <!-- Background Image (Ganti URL dengan gambar asli nanti) -->
  <div class="absolute inset-0 z-0 bg-[url('https://images.unsplash.com/photo-1542051841857-5f90071e7989?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80')] bg-cover bg-center"></div>

  <div class="container mx-auto px-6 relative z-20 text-center">
    <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
      Wujudkan Mimpi Bekerja & <br /> Sukses <span class="text-red-500"> di Jepang</span>
    </h1>
    <p class="text-lg md:text-xl mb-8 text-gray-200 max-w-2xl mx-auto">
      Lembaga Pelatihan dan Penempatan Tenaga Kerja Terpercaya untuk Program Magang & Tokutei Ginou.
    </p>
    <div class="flex flex-col md:flex-row justify-center gap-4">
      <a href="#pendidikan" class="bg-red-600 hover:bg-red-700 text-white px-8 py-3 rounded-lg font-bold transition flex items-center justify-center gap-2">
        Lihat Program <ArrowRight size={20} />
      </a>
      <a href="#kontak" class="bg-transparent border-2 border-white hover:bg-white hover:text-blue-900 text-white px-8 py-3 rounded-lg font-bold transition">
        Konsultasi Gratis
      </a>
    </div>
  </div>
</section>