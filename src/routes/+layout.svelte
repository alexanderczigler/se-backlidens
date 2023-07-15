<script>
	import Footer from '../components/Footer.svelte';
	import Top from '../sections/Top.svelte';

	export let segment;
</script>

<layout>
	<Top {segment} />
	<slot />
</layout>

<Footer />

<style>
	layout {
		position: relative;
		display: block;
		background-color: var(--lotion);
		padding-bottom: 5em;
	}

	@media (min-width: 800px) {
		layout {
		}
	}
</style>
