<script>
	import Nav from "../components/Nav.svelte";

	export let segment;
</script>

<layout>
	<Nav {segment} />

	<slot />
</layout>

<style>
	layout {
		position: relative;
		display: block;
	}

	@media (min-width: 800px) {
		layout {
		}
	}
</style>
