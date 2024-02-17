<template>
	<main class="bg-stone-200 dark:bg-gray-900 px-10 min-h-svh md:p-0 md:h-screen">
		<Navbar />
		<Card />
	</main>
</template>
<script setup lang="ts">
	import Navbar from './components/NavbarComponent.vue';
	import Card from './components/CardComponent.vue';
</script>
