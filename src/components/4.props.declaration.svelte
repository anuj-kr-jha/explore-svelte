
<!-- So far, we've dealt exclusively with internal state — that is to say, the values are only accessible within a given component. -->
<!--
  In any real application, you'll need to pass data from one component down to its children.
  To do that, we need to declare properties, generally shortened to 'props'.
  In Svelte, we do that with the export keyword. Edit the Nested.svelte component:
-->

<!--
  NOTE: Just like $:, this may feel a little weird at first. That's not how export normally works in JavaScript modules! Just roll with it for now
  it'll soon become second nature.
-->

<script lang="ts">
	export let answer1: number = 1; // default value
	export let answer2: number = 2; // default value
	export let answer3: number; // no default value
</script>

<p>The answer1 is {answer1}</p>
<p>The answer2 is {answer2}</p>
<p>The answer3 is {answer3}</p>