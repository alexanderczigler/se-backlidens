<script>
	import Logo from "./Logo.svelte";

	export let segment;
</script>

<nav>
	<Logo />

	<options>
		<ul>
			<li>
				<a aria-current={segment === undefined ? "page" : undefined} href="."
					>hem</a
				>
			</li>
			<li>
				<a aria-current={segment === "about" ? "page" : undefined} href="about"
					>katter</a
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
	</options>
</nav>

<style>
	nav {
		text-transform: uppercase;
		background-color: var(--lotion);
		height: 2em;
	}

	options {
		display: none;
	}

	@media (min-width: 800px) {
		nav {
			position: relative;
			display: block;
			top: 0em;
			width: 100%;
			padding: 1em 0;
			height: 2em;
		}

		options {
			display: block;
		}

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
