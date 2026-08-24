<script lang="ts">
	import { Menu, X } from 'lucide-svelte';
	let isOpen = $state(false);
</script>

<nav class="fixed z-50 w-full bg-linear-to-b from-white to-gray-100 shadow-md">
	<div class="container mx-auto flex items-center justify-between px-6 py-4">
		<!-- Logo -->
		<a href="/" class="text-2xl font-bold text-primary">
			LPK Artha
			<span class="bg-linear-to-r from-primary-light to-highlight bg-clip-text text-transparent"
				>Karier</span
			>
		</a>

		<!-- Desktop Menu -->
		<div class="hidden items-center space-x-8 md:flex">
			<a href="#pendidikan" class="font-medium text-gray-700 hover:text-primary">Pendidikan</a>
			<a href="#penempatan" class="font-medium text-gray-700 hover:text-primary">Penempatan</a>
			<a
				href="#kontak"
				class="rounded-full bg-linear-to-b from-highlight-light to-highlight px-5 py-2 font-medium text-primary transition hover:from-highlight hover:to-highlight-dark"
			>
				Daftar Sekarang
			</a>
		</div>

		<!-- Mobile Menu Button -->
		<button class="text-gray-700 md:hidden" onclick={() => (isOpen = !isOpen)}>
			{#if isOpen}
				<X />
			{:else}
				<Menu />
			{/if}
		</button>
	</div>

	<!-- Mobile Menu Dropdown -->
	{#if isOpen}
		<div
			class="flex flex-col space-y-4 border-t bg-linear-to-b from-white to-gray-50 p-4 shadow-lg md:hidden"
		>
			<a href="#pendidikan" class="font-medium text-gray-700" onclick={() => (isOpen = false)}
				>Pendidikan</a
			>
			<a href="#penempatan" class="font-medium text-gray-700" onclick={() => (isOpen = false)}
				>Penempatan</a
			>
			<a href="#kontak" class="font-bold text-primary" onclick={() => (isOpen = false)}
				>Daftar Sekarang</a
			>
		</div>
	{/if}
</nav>
