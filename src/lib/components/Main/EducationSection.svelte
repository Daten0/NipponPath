<script lang="ts">
  import { BookOpen, Users, Briefcase } from 'lucide-svelte';

  const programs = [
    {
      icon: BookOpen,
      title: "Bahasa Jepang Intensif",
      desc: "Kursus N5 hingga N3 dengan pengajar bersertifikat. Fokus percakapan sehari-hari dan teknis."
    },
    {
      icon: Users,
      title: "Budaya & Etos Kerja",
      desc: "Pelatihan tata krama (Reigi), disiplin waktu, dan budaya kerja Jepang agar cepat beradaptasi."
    },
    {
      icon: Briefcase,
      title: "Skill Teknis",
      desc: "Pelatihan dasar sesuai sektor: Manufaktur, Perawat Lansia (Kaigo), Pertanian, dan Konstruksi."
    }
  ];
</script>

<section id="pendidikan" class="py-20 bg-gray-50">
  <div class="container mx-auto px-6">
    <div class="text-center mb-16">
      <h2 class="text-3xl md:text-4xl font-bold text-blue-900 mb-4">Pendidikan & Pelatihan</h2>
      <div class="w-20 h-1 bg-red-600 mx-auto"></div>
      <p class="mt-4 text-gray-600 max-w-2xl mx-auto">
        Kami tidak hanya mengajarkan bahasa, kami membentuk karakter. Kurikulum kami dirancang khusus untuk mempersiapkan mental dan skill Anda.
      </p>
    </div>

    <div class="grid md:grid-cols-3 gap-8">
      {#each programs as program (program.title)}
        <div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition border-t-4 border-red-600">
          <div class="w-14 h-14 bg-blue-100 text-blue-900 rounded-full flex items-center justify-center mb-6">
            <program.icon size={28} />
          </div>
          <h3 class="text-xl font-bold text-gray-800 mb-3">{program.title}</h3>
          <p class="text-gray-600 leading-relaxed">{program.desc}</p>
        </div>
      {/each}
    </div>
  </div>
</section>