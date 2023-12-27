<script>
	/**
	 * @type {Array<{ title: string, id: string, type: string}>}
	 */
	export let restaurants = [];
</script>

<div class="bg-white shadow-md rounded-lg overflow-hidden">
	<table class="min-w-full">
		<thead>
			<tr>
				<th class="py-3 px-4 bg-gray-200 text-gray-700 font-semibold uppercase">Restaurant Name</th>
				<th class="py-3 px-4 bg-gray-200 text-gray-700 font-semibold uppercase">Restaurant Type</th>
				<th class="py-3 px-4 bg-gray-200 text-gray-700 font-semibold uppercase">Menu Link</th>
			</tr>
		</thead>
		<tbody>
			{#each restaurants as restaurant}
				<tr>
					<td class="py-3 px-4 border-b border-gray-200 text-black">{restaurant.title}</td>
					<td class="py-3 px-4 border-b border-gray-200 text-black">{restaurant.type}</td>
					<td class="py-3 px-4 border-b border-gray-200"
						><a href={`/menu/${restaurant.id}`} class="text-blue-500 hover:underline">Info</a></td
					>
				</tr>
			{/each}
		</tbody>
	</table>
</div>
