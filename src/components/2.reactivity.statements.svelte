<script lang="ts">
	let count = 0;

	function increment() {
		count += 1;
	}

	// We're not limited to declaring reactive values — we can also run arbitrary statements reactively. For example, we can log the value of count whenever it changes:
	$: console.log(`the count is ${count}`);

	// We can easily group statements together with a block:
	$: {
		console.log(`block: the count is ${count}`);
		console.log(`block: this will also be logged whenever count changes`);
  }


	// We can even put the $: in front of things like if blocks:
	$: if (count >= 10) {
		console.log('count is dangerously high!');
	}

</script>


<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>