<script>
	import Footer from '../components/Footer.svelte';
	import Top from '../sections/Top.svelte';
</script>

<layout>
	<Top />
	<slot />
</layout>
<div class="content">
	<Footer />
</div>

<style>
	div.content {
		drop-shadow: 0 0 1em var(--bokara-grey);
	}

	layout {
		position: relative;
		display: block;
		background-color: var(--white-smoke);
		padding-bottom: 5em;
	}

	/* @media (min-width: 800px) {
		layout {
		}
	} */
</style>
