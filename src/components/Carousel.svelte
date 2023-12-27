<script lang="ts">
	import { onMount } from 'svelte';

	type ImageType = {
		title: string;
		src: string;
	};

	export let images: ImageType[];

	let currentIndex = 0;

	onMount(() => {
		setInterval(() => {
			currentIndex = (currentIndex + 1) % images.length;
		}, 2000);
	});
</script>

<div class="carousel">
	{#each images as { title, src }, i}
		{#if i === currentIndex}
			<div class="text-center text-md mb-2">{title}?</div>
			<img class="carousel-image" {src} alt={title} />
		{/if}
	{/each}
</div>

<style>
	.carousel {
		display: flex-column;
		justify-content: center;
		align-items: center;
		height: 300px;
		overflow: hidden;
	}

	.carousel-image {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
