<script>
	import Footer from '../components/Footer.svelte';
	import Top from '../sections/Top.svelte';

	export let segment;
</script>

<layout>
	<Top {segment} />
	<slot />
</layout>
<div class="content">
	<Footer />
</div>

<style>
	div.content {
		margin: 0 auto;
		max-width: 800px;
		drop-shadow: 0 0 1em var(--shadow);
	}

	layout {
		position: relative;
		display: block;
		background-color: var(--guyabano);
		padding-bottom: 5em;
	}

	@media (min-width: 800px) {
		layout {
		}
	}
</style>
