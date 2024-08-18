<script>
	export let initialCount,
		maxCount = 10;
	let count = initialCount;

	function increment() {
		count++;
		count = Math.min(maxCount, count);
	}
</script>

<button on:click={increment}>Clicks {count}</button>

<style>
	button {
		padding: 2rem;
	}
</style>
