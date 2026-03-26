<script lang="ts">
  import { MapPin, Phone, Mail } from 'lucide-svelte';
</script>

<footer id="kontak" class="bg-blue-900 text-white pt-16 pb-8">
  <div class="container mx-auto px-6">
    <div class="grid md:grid-cols-3 gap-12 mb-12">
      <!-- Brand -->
      <div>
        <h3 class="text-2xl font-bold mb-4">Nippon<span class="text-red-500">Pathway</span></h3>
        <p class="text-gray-300 leading-relaxed">
          Mitra terpercaya Anda untuk meraih karir impian di Jepang dengan proses yang legal, aman, dan terjamin.
        </p>
      </div>

      <!-- Kontak -->
      <div>
        <h4 class="text-lg font-bold mb-4 border-b border-gray-600 inline-block pb-2">Hubungi Kami</h4>
        <ul class="space-y-3">
          <li class="flex items-start gap-3">
            <MapPin size={20} class="text-red-500 mt-1" />
            <span class="text-gray-300">Jl. Perdata Poros Blok E No. 3 Makassar, Indonesia</span>
          </li>
          <li class="flex items-center gap-3">
            <Phone size={20} class="text-red-500" />
            <span class="text-gray-300">+6287822462237 (Direktur NipponMaru)</span>
          </li>
          <li class="flex items-center gap-3">
            <Mail size={20} class="text-red-500" />
            <span class="text-gray-300">squantuminstitute@gmail.com</span>
          </li>
        </ul>
      </div>

      <!-- Links -->
      <div>
        <h4 class="text-lg font-bold mb-4 border-b border-gray-600 inline-block pb-2">Tautan</h4>
        <ul class="space-y-2">
          <li><a href="#pendidikan" class="text-gray-300 hover:text-white transition">Program Pendidikan</a></li>
          <li><a href="#penempatan" class="text-gray-300 hover:text-white transition">Proses Penempatan</a></li>
          <li><a href="#" class="text-gray-300 hover:text-white transition">Syarat & Ketentuan</a></li>
        </ul>
      </div>
    </div>

    <div class="border-t border-gray-700 pt-8 text-center text-gray-400 text-sm">
      &copy; {new Date().getFullYear()} Nippon Pathway. All rights reserved.
    </div>
  </div>
</footer>