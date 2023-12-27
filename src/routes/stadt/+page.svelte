<script>
	import ButtonClick from '../../components/ButtonClick.svelte';
	import Youtube from '../../components/Youtube.svelte';

	let city = '';
	let counter = 0;
	let output = '';

	function handleSubmit() {
		if (city.toLowerCase() === 'wien') {
			output = 'Okaaay, lets go!';
		} else {
			counter++;
		}
	}
</script>

<h1 class="text-3xl mb-4 text-center">Wohin fahren wir denn nun...</h1>
<div class="justify-center">
	<form on:submit|preventDefault={handleSubmit} class="flex justify-center">
		<input
			type="text"
			class="text-black pl-2 rounded-md mr-2"
			bind:value={city}
			placeholder="Stadt eingeben"
		/>
		<button type="submit" class="rounded bg-blue-500 hover:bg-blue-700 text-white text-lg py-1 px-3"
			>Submit</button
		>
	</form>

	<div class="flex flex-col justify-center items-center mt-4x">
		<div class="flex-col">
			{#if output === ''}
				{#if counter > 0}
					<p>Tipp Box</p>
				{/if}
				{#if counter > 0}
					<p>Versuche: {counter}</p>
				{/if}
				{#if counter > 2}
					<p class="">Tipp: Lukas wohnt in der Stadt</p>
				{/if}
				{#if counter > 4}
					<p class="text-green text-5xl">Wien...</p>
				{/if}
			{:else}
				<p class=""></p>
			{/if}
		</div>
		<div class="flex-col">
			{#if output != ''}
				<p class="text-red-500 text-5xl mt-10 text-center mb-4">{output}</p>
				<Youtube videoId="AWM5ZNdWlqw" title="Lets go!" />
				<div class="mx-auto mt-5 lg:">
					<ButtonClick title="Go to Wien" link="/essen" />
				</div>
			{/if}
		</div>
	</div>
</div>
