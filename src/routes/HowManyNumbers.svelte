<script lang="ts">
	export let inputHowManyNumbers: number;
</script>

<div class="form-control">
	<!-- svelte-ignore a11y-label-has-associated-control -->
	<label class="label">
		<span class="label-text">Enter how many numbers to generate</span>
	</label>
	<label class="input-group">
		<span class="w-24">Number:</span>
		<input
			type="text"
			placeholder="10"
			required
			bind:value={inputHowManyNumbers}
			class="input input-bordered w-56"
		/>
	</label>
</div>
