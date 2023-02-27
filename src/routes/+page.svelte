<script>
	// @ts-nocheck

	import HowManyNumbers from './HowManyNumbers.svelte';
	import RangeOfNumbers from './RangeOfNumbers.svelte';
	import SortSpeed from './SortSpeed.svelte';
	import ButtonHandler from './ButtonHandler.svelte';

	let howManyNumbers = '';
	let rangeOfNumbers = '';
	let selectSortSpeedOption = '';

	$: howManyNumbers = howManyNumbers;
	$: rangeOfNumbers = rangeOfNumbers;
	$: sortSpeedOption = selectSortSpeedOption;
</script>

<div class="flex h-screen">
	<div class="m-auto">
		<HowManyNumbers bind:inputHowManyNumbers={howManyNumbers} />
		<RangeOfNumbers bind:inputRangeOfNumbers={rangeOfNumbers} />
		<SortSpeed bind:sortSpeedOption={selectSortSpeedOption} />
		<ButtonHandler />
		<p>How many Numbers: {howManyNumbers}</p>
		<p>Range of Numbers: {rangeOfNumbers}</p>
		<p>Sort speed option: {sortSpeedOption ? sortSpeedOption.text : ''}</p>
	</div>
</div>
