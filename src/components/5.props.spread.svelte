<script>
	export let name;
	export let version;
	export let speed;
	export let website;
	let x = 1;

	$: href = `https://www.npmjs.com/package/${name}`;
</script>

<p>
	The <code>{name}</code> package is {speed} fast. Download version {version} from
	<a {href}>npm</a> and <a href={website}>learn more here</a>
</p>


<!--
	Conversely, if you need to reference all the props that were passed into a component, including ones that weren't declared with export,
	WARNING : we can do so by accessing $$props directly. It's not generally recommended, as it's difficult for Svelte to optimizes, but it's useful in rare cases.
-->
<!-- <p>{JSON.stringify($$props)}</p> -->

