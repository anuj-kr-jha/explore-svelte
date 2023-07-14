<!-- FOR ARRAY -->

<!--
<script lang="ts">
	let numbers = [1, 2, 3, 4];

function addNumber() {
	// numbers = [...numbers, numbers.length + 1];
	numbers[numbers.length] = numbers.length + 1;
}

$: sum = numbers.reduce((total, currentNumber) => total + currentNumber, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>
-->




<!--
	Because Svelte's reactivity is triggered by assignments, using array methods like push and splice won't automatically cause updates.
	For example, clicking the 'Add a number' button doesn't currently do anything, even though we're calling numbers.push(...) inside addNumber.

	One way to fix that is to add an assignment that would otherwise be redundant:

	```javaScript
	function addNumber() {
		numbers.push(numbers.length + 1);
		numbers = numbers;
	}
	```

	But there's a more idiomatic solution:
		```javaScript
	function addNumber() {
		numbers.push(numbers.length + 1);
		numbers = numbers;
	}
	```

	We can use similar patterns to replace pop, shift, unshift and splice.
 -->


 <!-- FOR OBJECTS -->

<script lang="ts">
	const object = {count: 1};

	function increment() {
		object.count += 1;
	}

</script>

<p>{JSON.stringify(object)}</p>

<button on:click={increment}>
	Add a number
</button>