<script lang="ts">
	let count1 = 0;
	let count2 = 0;

	function increment1() {
		count1 += 1;
	}
	function increment2() {
		count2 += 1;
	}
</script>

<button on:click={increment1}>
	Clicked {count1}
	{count1 === 1 ? 'time' : 'times'}
</button>

<button on:click={increment2}>
	Clicked {count2}
	{count2 === 1 ? 'time' : 'times'}
</button>