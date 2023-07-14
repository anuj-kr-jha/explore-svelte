<script lang="ts">
	import ReactivityDeclaration from './components/1.reactivity.declaration.svelte';
	import ReactivityStatements from './components/2.reactivity.statements.svelte';
	import ReactivityArrayAndObject from './components/3.reactivity.arrayAndObject.svelte';
	//
	import PropsDeclaration from './components/4.props.declaration.svelte';
	import PropsSpread from './components/5.props.spread.svelte';

	const pkg = {
		name: 'svelte',
		speed: 'blazing',
		version: 4,
		website: 'https://svelte.dev'
	};

</script>

<!-- Reactivity -->
<!--
<ReactivityDeclaration />
<ReactivityStatements />
<ReactivityArrayAndObject />
 -->

 <!-- PROPS -->
<PropsDeclaration answer1={42} answer2={23} answer3={34} /> <!-- passing data to component while using it. It is like calling function with values-->
<PropsDeclaration answer3={3}/> <!-- calling data without data. default will be used if specified-->
<!--
<PropsSpread
	name={pkg.name}
	speed={pkg.speed}
	version={pkg.version}
	website={pkg.website}
/>
-->
<!-- this will also work -->
<PropsSpread {...pkg}/>