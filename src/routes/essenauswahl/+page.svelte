<script>
	import ButtonClick from '../../components/ButtonClick.svelte';
	import TableMenu from '../../components/TableMenu.svelte';

	let restaurants = [
		{ title: 'Ferhat Döner', id: 'ferhat/5dztSqADB5U', type: 'Döner' },
		{ title: 'Kvetch Burger', id: 'kvetch/jwdVQ8xuaRE', type: 'Burger' },
		{ title: 'Demel', id: 'demel/NJNRqCRK-do', type: 'Kaiserschmarn' },
		{ title: 'Wienerschnitzel', id: 'Wienerschnitzel/xag2GeQId2Q', type: 'Schnitzel' },
		{ title: 'Wiener Würstl Stand', id: 'wuerstl/NJNRqCRK-do', type: 'Woscht :)' }
	];
</script>

<div>
	<h1 class="text-3xl mb-10 text-center font-semibold uppercase">
		Wilkommen zu deinem Food-Guide!
	</h1>
	<TableMenu {restaurants} />
	<ButtonClick title="Datum Auswählen" link="/datum" />
</div>
