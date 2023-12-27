<script>
	// @ts-nocheck

	import { onMount } from 'svelte';
	import ButtonClick from '../../components/ButtonClick.svelte';

	/**
	 * @type {null}
	 */
	let selectedDate = null;

	onMount(() => {
		// Initialize date picker here
	});

	/**
	 * @param {{ target: { value: string; }; }} event
	 */
	function handleDateChange(event) {
		selectedDate = event.target.value;
	}
</script>

<h1 class="text-4xl font-bold mb-4 text-center">Datum</h1>

<div class="flex items-center flex-col">
	<label for="datepicker" class="mr-2">Select a date:</label>
	<input
		type="date"
		id="datepicker"
		class="border border-gray-300 rounded px-2 py-1 text-black"
		on:change={handleDateChange}
		bind:value={selectedDate}
	/>

	{#if selectedDate}
		<p class="mt-4">Selected date: {selectedDate}</p>
	{/if}

	<ButtonClick title="Submit" link="/ergebnis/{selectedDate}" />
</div>
