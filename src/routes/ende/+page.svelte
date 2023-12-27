<script>
	function downloadImage() {
		const link = document.createElement('a');
		link.href = 'src/lib/wien.png';
		link.download = 'wien.png';
		link.click();
	}
</script>

<div style="display: flex; flex-direction: column; align-items: center;">
	<div style="flex: 1;">
		<img src="src/lib/wien.png" alt="wien" class="w-2/5 mx-auto" />
	</div>
	<div class="flex mt-5 rounded">
		<button
			on:click={downloadImage}
			class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600">Download Coupon</button
		>
	</div>
</div>
