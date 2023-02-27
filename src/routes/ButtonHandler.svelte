<script>
	let count = 0;

	const increment = () => {
		count += 1;
	};
</script>

<div class="form-control flex flex-col items-center">
	<!-- svelte-ignore a11y-label-has-associated-control -->
	<label class="label" />
	<button class="btn w-24" on:click={increment}> Sort {count} </button>
</div>
