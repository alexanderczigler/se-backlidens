<script>
	export let segment;
</script>

<nav>
	<ul>
		<li>
			<a aria-current={segment === undefined ? "page" : undefined} href="."
				>hem</a
			>
		</li>
		<li>
			<a aria-current={segment === "about" ? "page" : undefined} href="about"
				>våra katter</a
			>
		</li>
		<li>
			<a aria-current={segment === "about" ? "page" : undefined} href="about"
				>kullar</a
			>
		</li>
		<li>
			<a aria-current={segment === "about" ? "page" : undefined} href="about"
				>utställningar</a
			>
		</li>
	</ul>
</nav>

<style>
	nav {
		float: right;
		width: 45%;
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: "";
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
		font-weight: 600;
		color: var(--falu);
		border-bottom: 1px solid var(--falu);
	}

	a {
		text-decoration: none;
		padding: 0.5em 0.5em;
		display: block;
	}
</style>
