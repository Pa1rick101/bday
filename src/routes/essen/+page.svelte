<script>
	import ButtonClick from '../../components/ButtonClick.svelte';
	import Carousel from '../../components/Carousel.svelte';
	export const prerender = true;

	let images = [
		{ title: 'Döner', src: 'src/lib/doener.png' },
		{ title: 'Pizza', src: 'src/lib/pizza.png' },
		{ title: 'Burger', src: 'src/lib/burger.png' },
		{ title: 'Schnitzel', src: 'src/lib/schnitzel.png' }
	];
</script>

<section class="flex flex-col items-center">
	<h1 class="text-3xl mb-4 text-center">Wilkommen zu deinem Food-Guide!</h1>
	<Carousel {images} />
	<ButtonClick title="Essen Auswählen" link="/essenauswahl" />
</section>
