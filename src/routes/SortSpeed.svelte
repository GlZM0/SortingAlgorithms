<script>
	import SortSpeedOptions from './SortSpeedOptions.svelte';

	export let speed = [
		{ id: 1, text: 'Slow' },
		{ id: 2, text: 'Normal' },
		{ id: 3, text: 'Fast' },
		{ id: 4, text: 'Very Fast' },
		{ id: 5, text: 'I am speed' }
	];

	/**
	 * @type {any}
	 */
	export let sortSpeedOption;
</script>

<div class="form-control">
	<!-- svelte-ignore a11y-label-has-associated-control -->
	<label class="label">
		<span class="label-text">Choose the sort speed</span>
	</label>
	<!-- svelte-ignore a11y-label-has-associated-control -->
	<label class="input-group">
		<span class="w-24">Speed:</span>
		<SortSpeedOptions {speed} bind:selectedSortSpeedOption={sortSpeedOption} />
	</label>
</div>
