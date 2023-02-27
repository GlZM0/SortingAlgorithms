<script>
	/**
	 * @type {any}
	 */
	export let selectedSortSpeedOption;
	/**
	 * @type {any}
	 */
	export let speed;

	let placeholder = 'Select the speed';
</script>

<select required bind:value={selectedSortSpeedOption} class="select select-bordered max-w-xs w-56">
	{#if placeholder}
		<option value="" disabled selected>{placeholder}</option>
	{/if}
	{#each speed as spd}
		<option value={spd}>{spd.text}</option>
	{/each}
</select>
