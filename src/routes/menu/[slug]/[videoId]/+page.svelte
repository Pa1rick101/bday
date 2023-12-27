<script>
	import { page } from '$app/stores';
	import ButtonClick from '../../../../components/ButtonClick.svelte';
	import Youtube from '../../../../components/Youtube.svelte';

	let slug = $page.params.slug;
	let videoId = $page.params.videoId;
</script>

<div>
	<h1 class="text-3xl text-center mb-5">{slug.toUpperCase()}</h1>
	<Youtube {videoId} title={slug} />
	<ButtonClick title="Zurück" link="/essenauswahl" />
</div>
