<template>
	<nav class="flex items-center p-10 mb-5 justify-end md:justify-around md:mb-10">
		<span class="text-left"></span>
		<button
			class="w-10 relative rounded-lg h-6 border-solid border-red-900 bg-transparent transition-all"
		>
			<span @click="changeTheme">
				<Sun v-if="dark" />
				<Moon v-else />
			</span>
		</button>
	</nav>
</template>
<script lang="ts" setup>
	import { onMounted } from 'vue';
	import { Sun, Moon } from './images';
	import { useDark } from '../composables/useDark';

	const { changeTheme, loadDarkMode, dark } = useDark();

	onMounted(() => {
		loadDarkMode();
	});
</script>
