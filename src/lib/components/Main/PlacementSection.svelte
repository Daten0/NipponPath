<script lang="ts">
  import { FileText, Video, Plane, Handshake } from 'lucide-svelte';

  const steps = [
    { icon: FileText, title: "Seleksi Admin", desc: "Pendaftaran & Screening berkas awal." },
    { icon: Video, title: "Wawancara User", desc: "Interview dengan perusahaan Jepang (Online/Offline)." },
    { icon: Handshake, title: "Pelatihan & Visa", desc: "Pelatihan intensif dan pengurusan COE/Visa." },
    { icon: Plane, title: "Pemberangkatan", desc: "Pendampingan hingga tiba di Bandara Jepang." }
  ];
</script>

<section id="penempatan" class="py-20 bg-white">
  <div class="container mx-auto px-6">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-bold text-blue-900 mb-4">Proses Penempatan</h2>
      <div class="w-20 h-1 bg-red-600 mx-auto"></div>
      <p class="mt-4 text-gray-600">
        Transparan dan Terjamin. Kami memproses dokumen visa Anda dengan legalitas yang jelas.
      </p>
    </div>

    <div class="grid md:grid-cols-4 gap-6">
      {#each steps as step, index (step.title)}
        <div class="relative flex flex-col items-center text-center">
          <!-- Connector Line (Desktop Only) -->
          {#if index < steps.length - 1}
            <div class="hidden md:block absolute top-8 left-1/2 w-full h-0.5 bg-gray-200 -z-10"></div>
          {/if}
          
          <div class="w-16 h-16 bg-blue-900 text-white rounded-full flex items-center justify-center mb-4 shadow-lg z-10">
            <step.icon size={24} />
          </div>
          <h3 class="text-lg font-bold text-gray-800 mb-2">{step.title}</h3>
          <p class="text-sm text-gray-500">{step.desc}</p>
        </div>
      {/each}
    </div>
    
    <!-- Mitra Section -->
    <div class="mt-20 text-center">
      <p class="text-gray-500 mb-6 font-medium">DIPERCAYA OLEH PERUSAHAAN JEPANG</p>
      <div class="flex flex-wrap justify-center gap-8 opacity-60 grayscale hover:grayscale-0 transition duration-500">
        <!-- Placeholder Logo Mitra -->
        <div class="h-10 w-32 bg-gray-300 rounded"></div>
        <div class="h-10 w-32 bg-gray-300 rounded"></div>
        <div class="h-10 w-32 bg-gray-300 rounded"></div>
        <div class="h-10 w-32 bg-gray-300 rounded"></div>
      </div>
    </div>
  </div>
</section>