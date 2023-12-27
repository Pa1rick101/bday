<script>
	import { page } from '$app/stores';
	import ButtonClick from '../../../components/ButtonClick.svelte';
	import Youtube from '../../../components/Youtube.svelte';

	let datum = $page.params.slug;

	/**
	 * @param {string | number | Date} datum
	 */
	function formatDate(datum) {
		const date = new Date(datum);
		const day = date.getDate();
		const month = date.getMonth() + 1;
		const year = date.getFullYear();

		return `${day < 10 ? '0' + day : day}.${month < 10 ? '0' + month : month}.${year}`;
	}

	let formattedDate = formatDate(datum);
</script>

<div>
	<h1 class="text-3xl text-center mb-5">{formattedDate}</h1>
	<Youtube title="kaffee" videoId="8h--YHE5rWQ" />
	<ButtonClick title="Lets gooo!" link="/ende" />
</div>
