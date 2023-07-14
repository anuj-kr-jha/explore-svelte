<script lang="ts">
  import src from './assets/svelte.svg';
  import Nested from './Nested.svelte';
	import HtmlTag from './HtmlTag.svelte';
  let name = 'svelte';
</script>

<main>
<p>welcome to svelte</p>
<img src={src} alt={name} />
<img {src} alt="svelte" /> <!--It's not uncommon to have an attribute where the name and value are the same, like src={src}. Svelte gives us a convenient shorthand for these cases-->
</main>

<Nested /> <!-- Notice that even though Nested.svelte has a <p> element, the styles from App.svelte don't leak in. -->

<HtmlTag />

<style>
	p {
		color: goldenrod;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>
