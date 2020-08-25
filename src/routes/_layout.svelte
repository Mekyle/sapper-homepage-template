<script>
	import Tailwindcss from '../components/Tailwindcss.svelte';
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	main {
		background-color: white;
	}
</style>

<Tailwindcss />

<Nav {segment}/>

<main>
	<slot></slot>
</main>