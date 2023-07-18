<script lang="ts">
	export let onClick = () => {};

	import { page } from '$app/stores';
</script>

<nav>
	<ul>
		<li>
			<a on:click={onClick} aria-current={$page.url.pathname === '/' ? 'page' : undefined} href="."
				>om</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={$page.url.pathname === '/litters' ? 'page' : undefined}
				href="litters">kattungar</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={$page.url.pathname === '/shows' ? 'page' : undefined}
				href="shows">utställningar</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={$page.url.pathname === '/links' ? 'page' : undefined}
				href="links">länkar</a
			>
		</li>
	</ul>
</nav>

<style>
	ul {
		list-style-type: none;
	}

	li {
		color: var(--white-smoke);
		font-size: 2.6em;
		text-transform: uppercase;
	}

	[aria-current] {
		font-weight: 600;
		color: var(--white-smoke);
	}

	a {
		text-decoration: none;
		padding: 0 0.5em;
		display: block;
	}

	@media (min-width: 800px) {
		ul {
			float: right;
			margin: 0.3em 1em 0 0;
			padding: 0;
		}

		/* clearfix */
		ul::after {
			content: '';
			display: block;
			clear: both;
		}

		li {
			color: var(--desert);
			font-weight: 100;
			font-size: 1em;
			display: block;
			float: left;
		}

		[aria-current] {
			font-weight: 400;
			color: var(--white-smoke);
			background-color: var(--desert);
		}

		a {
			text-decoration: none;
			padding: 0.1em 0.5em 0 0.5em;
			display: block;
			border-radius: 0.1em;
		}
	}
</style>
