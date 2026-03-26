<script lang="ts">
  import { Menu, X } from 'lucide-svelte';
  let isOpen = false;
</script>

<nav class="bg-white shadow-md fixed w-full z-50">
  <div class="container mx-auto px-6 py-4 flex justify-between items-center">
    <!-- Logo -->
    <a href="/" class="text-2xl font-bold text-blue-900">
      Nippon<span class="text-red-600">Pathway</span>
    </a>

    <!-- Desktop Menu -->
    <div class="hidden md:flex space-x-8 items-center">
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#pendidikan" class="text-gray-700 hover:text-blue-900 font-medium">Pendidikan</a>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#penempatan" class="text-gray-700 hover:text-blue-900 font-medium">Penempatan</a>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#kontak" class="bg-red-600 text-white px-5 py-2 rounded-full font-medium hover:bg-red-700 transition">
        Daftar Sekarang
      </a>
    </div>

    <!-- Mobile Menu Button -->
    <button class="md:hidden text-gray-700" on:click={() => isOpen = !isOpen}>
      {#if isOpen}
        <X />
      {:else}
        <Menu />
      {/if}
    </button>
  </div>

  <!-- Mobile Menu Dropdown -->
  {#if isOpen}
    <div class="md:hidden bg-white border-t p-4 flex flex-col space-y-4 shadow-lg">
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#pendidikan" class="text-gray-700 font-medium" on:click={() => isOpen = false}>Pendidikan</a>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#penempatan" class="text-gray-700 font-medium" on:click={() => isOpen = false}>Penempatan</a>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#kontak" class="text-red-600 font-bold" on:click={() => isOpen = false}>Daftar Sekarang</a>
    </div>
  {/if}
</nav>