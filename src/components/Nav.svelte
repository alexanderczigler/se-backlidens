<script>
	export let segment;
	export let toggleMenu;
</script>

<nav>
	<ul>
		<li>
			<a
				on:click={toggleMenu}
				aria-current={segment === undefined ? "page" : undefined}
				href=".">hem</a
			>
		</li>
		<li>
			<a
				on:click={toggleMenu}
				aria-current={segment === "cats" ? "page" : undefined}
				href="cats">katter</a
			>
		</li>
		<li>
			<a
				on:click={toggleMenu}
				aria-current={segment === "litters" ? "page" : undefined}
				href="litters">kullar</a
			>
		</li>
		<li>
			<a
				on:click={toggleMenu}
				aria-current={segment === "shows" ? "page" : undefined}
				href="shows">utställningar</a
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
		font-weight: 400;
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
			font-weight: 600;
			color: var(--falu);
		}

		a {
			text-decoration: none;
			padding: 0 0.5em;
			display: block;
		}
	}
</style>
