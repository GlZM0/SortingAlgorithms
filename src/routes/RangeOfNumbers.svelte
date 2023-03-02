<script lang="ts">
	export let inputRangeOfNumbers: number;
</script>

<div class="form-control">
	<!-- svelte-ignore a11y-label-has-associated-control -->
	<label class="label">
		<span class="label-text">Write the range of numbers:</span>
	</label>
	<label class="input-group">
		<span class="w-24">Range:</span>
		<input
			type="text"
			required
			bind:value={inputRangeOfNumbers}
			placeholder="10"
			class="input input-bordered w-56"
		/>
	</label>
</div>
