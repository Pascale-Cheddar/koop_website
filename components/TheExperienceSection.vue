<script setup lang="ts">
	import skills from '../assets/skills/skills.json';
</script>

<style></style>

<template>
	<section
		class="experience mx-5"
		id="experience-section">
		<h2 class="title section-title mt-24">{{ $t('sectionTitles.experience') }}</h2>
		<div class="lg:flex lg:mt-14">
			<img
				class="hidden lg:block rounded-lg lg:shadow-image"
				src="/experience-desktop.webp"
				width="400"
				height="600"
				alt="A picture of Pascal outside near water in summer" />
			<div class="grid justify-center grid-cols-2 gap-9 mt-14 mx-auto grid-flow-dense max-w-fit">
				<div
					v-for="skill in skills"
					:key="skill.name"
					class="skill flex flex-row">
					<NuxtLink
						:to="skill.link"
						class="flex" target="_blank">
						<img
							:src="skill.image"
							:alt="skill.alt"
							:width="48"
							:height="48"
							class="skill-img mr-4 h-[3rem] grayscale hover:grayscale-0 transition-all duration-300 ease-in hover:-translate-y-1 hover:-translate-x-1" />
						<h3 class="font-rota text-[1rem] uppercase">{{ skill.name }}</h3>
					</NuxtLink>
				</div>
			</div>
		</div>
	</section>
</template>
