<script>
	/**
	 * @type {string}
	 */
	export let videoId;
	/**
	 * @type {string}
	 */
	export let title;
</script>

<iframe
	{title}
	width="560"
	height="315"
	src={`https://www.youtube.com/embed/${videoId}`}
	frameborder="0"
	allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
	allowfullscreen
></iframe>
