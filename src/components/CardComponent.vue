<template>
	<div
		class="flex flex-col items-center sm:my-10 bg-slate-100 max-w-md m-auto p-10 rounded-md shadow-md gap-2 dark:bg-slate-800"
	>
		<Profile />
		<h1 class="text-2xl text-center font-bold dark:text-slate-50">
			Federico Daniel Martinez
		</h1>
		<p class="dark:text-stone-300">Buenos Aires, Argentina</p>

		<span class="mt-5 dark:text-stone-400 text-center"
			>"Front-end developer and I'm a beliver"</span
		>

		<div class="flex w-full mt-2" v-for="socialInfo in SocialMediaLink">
			<a
				:href="socialInfo.url"
				target="_blank"
				class="text-md bg-indigo-100 rounded w-full font-semibold text-center p-2 hover:opacity-85 dark:text-slate-200 dark:bg-slate-500"
			>
				{{ socialInfo.title }}
			</a>
		</div>
	</div>
</template>

<script setup lang="ts">
	import { Profile } from './images';
	import { SocialMediaLink } from '../data/Links';
</script>
