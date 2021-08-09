<script>
	import Logo from "./Logo.svelte";

	export let segment;

	let overlay = false;
	const toggleMenu = () => {
		overlay = !overlay;
	};
</script>

{#if overlay}
	<overlay>
		<h3>Meny</h3>
		<ul>
			<li>
				<a aria-current={segment === undefined ? "page" : undefined} href="."
					>hem</a
				>
			</li>
			<li>
				<a aria-current={segment === "cats" ? "page" : undefined} href="cats"
					>katter</a
				>
			</li>
			<li>
				<a
					aria-current={segment === "litters" ? "page" : undefined}
					href="litters">kullar</a
				>
			</li>
			<li>
				<a aria-current={segment === "shows" ? "page" : undefined} href="shows"
					>utställningar</a
				>
			</li>
		</ul>
	</overlay>
{/if}

<nav>
	<Logo />

	<hamburger>
		<span>
			<i class="fa fa-bars" on:click={toggleMenu} />
		</span>
	</hamburger>

	<options>
		<ul>
			<li>
				<a aria-current={segment === undefined ? "page" : undefined} href="."
					>hem</a
				>
			</li>
			<li>
				<a aria-current={segment === "cats" ? "page" : undefined} href="cats"
					>katter</a
				>
			</li>
			<li>
				<a
					aria-current={segment === "litters" ? "page" : undefined}
					href="litters">kullar</a
				>
			</li>
			<li>
				<a aria-current={segment === "shows" ? "page" : undefined} href="shows"
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
		height: 5em;
	}

	overlay {
		display: block;
		position: absolute;
		height: 100%;
		width: 100%;
		top: 5em;
		background-color: var(--falu);
		z-index: 10;
	}

	options {
		display: none;
	}

	hamburger {
		float: right;
	}

	hamburger > span > i {
		font-size: 2em;
		padding-right: 0.9em;
		padding-top: 0.7em;
	}

	@media (min-width: 800px) {
		hamburger {
			display: none;
		}

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
