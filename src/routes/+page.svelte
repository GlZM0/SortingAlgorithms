<script>
	// @ts-nocheck

	import HowManyNumbers from './HowManyNumbers.svelte';
	import RangeOfNumbers from './RangeOfNumbers.svelte';
	import SortSpeed from './SortSpeed.svelte';

	let howManyNumbers = '';
	let rangeOfNumbers = '';
	let selectSortSpeedOption = '';

	$: howManyNumbers = howManyNumbers;
	$: rangeOfNumbers = rangeOfNumbers;
	$: sortSpeedOption = selectSortSpeedOption;

	const hideFunction = () => {
		var optionBar = document.getElementById('optionBar');
		optionBar.classList.add('hidden');
	};
</script>

<div class="h-screen relative justify-center z-0 flex bg-gray-500 items-center">
	<div class="border-solid border-4 bg-gray-300">
		<p class="p-16 text-blue-400">asdasd</p>
	</div>
	<div
		class="border-solid border-4 absolute bg-gray-600 border-gray-800 rounded-md z-10"
		id="optionBar"
	>
		<div class="relative">
			<button
				class="rounded-md p-2 absolute top-0 right-0 text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-gray-400"
				on:click={hideFunction}
			>
				<span class="sr-only">Close menu</span>
				<!-- Heroicon name: outline/x -->
				<svg
					class="h-6 w-6"
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					aria-hidden="true"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M6 18L18 6M6 6l12 12"
					/>
				</svg>
			</button>
		</div>
		<div class="p-16">
			<HowManyNumbers bind:inputHowManyNumbers={howManyNumbers} />
			<RangeOfNumbers bind:inputRangeOfNumbers={rangeOfNumbers} />
			<SortSpeed bind:sortSpeedOption={selectSortSpeedOption} />
			<p>How many Numbers: {howManyNumbers}</p>
			<p>Range of Numbers: {rangeOfNumbers}</p>
			<p>Sort speed option: {sortSpeedOption ? sortSpeedOption.text : ''}</p>
		</div>
	</div>
</div>
