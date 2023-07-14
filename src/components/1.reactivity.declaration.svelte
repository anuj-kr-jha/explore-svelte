<script lang="ts">
	let count = 0;
	// let double = count*2; // this will not update when count changes
	// some parts of a component's state need to be computed from other parts for that we need to use reactive declarations

	$: double = count * 2; // this will update when count changes

	function increment() {
		count += 1;
	}

</script>

<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {double}</p>
<!-- Of course, you could just write {count * 2} in the markup instead — you don't have to use reactive values. Reactive values become particularly valuable (no pun intended) when you need to reference them multiple times, or you have values that depend on other reactive values. -->
<p>{count} doubled is {count*2}</p>

<!-- Note that reactive declarations and statements will run after other script code and before component markup is rendered. -->