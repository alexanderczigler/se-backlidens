<script>
	export let segment;
	export let onClick;
</script>

<nav>
	<ul>
		<li>
			<a
				on:click={onClick}
				aria-current={segment === undefined ? "page" : undefined}
				href=".">om</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={segment === "litters" ? "page" : undefined}
				href="litters">kattungar</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={segment === "shows" ? "page" : undefined}
				href="shows">utställningar</a
			>
		</li>
		<li>
			<a
				on:click={onClick}
				aria-current={segment === "links" ? "page" : undefined}
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
		color: var(--lotion);
		font-size: 2.6em;
		text-transform: uppercase;
		text-align: right;
	}

	[aria-current] {
		font-weight: 600;
		color: var(--grayscale);
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
			content: "";
			display: block;
			clear: both;
		}

		li {
			color: var(--grayscale);
			font-weight: 100;
			font-size: 1em;
			display: block;
			float: left;
		}

		[aria-current] {
			font-weight: 400;
			color: var(--falu);
		}

		a {
			text-decoration: none;
			padding: 0 0.5em;
			display: block;
		}
	}
</style>
