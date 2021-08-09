<script>
	import Top from "../sections/Top.svelte";
	import Nav from "../components/Nav.svelte";

	export let segment;
</script>

<layout>
	<Top {segment} />

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
