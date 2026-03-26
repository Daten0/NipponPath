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
  <section class="py-16 bg-red-600 text-white text-center">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold mb-4">Siap Memulai Perjalanan Anda?</h2>
      <p class="mb-8 text-red-100">Konsultasikan kondisi Anda dengan ahli kami secara gratis.</p>
      <a href="https://wa.me/6287822462237" target="_blank" class="bg-white text-red-600 px-8 py-3 rounded-full font-bold hover:bg-gray-100 transition inline-block">
        Chat WhatsApp Sekarang
      </a>
    </div>
  </section>
</main>
