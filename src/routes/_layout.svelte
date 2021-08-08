<script>
	import Nav from "../components/Nav.svelte";

	export let segment;
</script>

<layout>
	<Nav {segment} />

	<!-- <hr />

	<main>
		<slot />
	</main> -->
</layout>

<style>
	layout {
		position: relative;
		display: block;
	}

	hr {
		border: 0;
		height: 1px;
		background-image: linear-gradient(
			to right,
			rgba(0, 0, 0, 0),
			rgba(0, 0, 0, 0.1),
			rgba(0, 0, 0, 0)
		);
	}

	main {
		display: block;
		top: 4em;
		margin: 1em 1em;
	}

	@media (min-width: 800px) {
		layout {
		}
	}
</style>
