<script>
	import Logo from '../components/Logo.svelte';
	import Nav from '../components/Nav.svelte';

	let overlay = false;
	const toggleMenu = () => {
		overlay = !overlay;
	};
</script>

{#if overlay}
	<overlay>
		<Nav onClick={toggleMenu} />
	</overlay>
{/if}

<top>
	<hamburger>
		<span>
			<i
				class="fa fa-bars"
				class:fa-times={overlay}
				on:click={toggleMenu}
				on:keyup={toggleMenu}
				role="button"
				tabindex="0"
			/>
		</span>
	</hamburger>

	<Logo />

	<options>
		<Nav onClick={() => {}} />
	</options>
</top>

<style>
	top {
		display: block;
		text-transform: uppercase;
		background-color: var(--white-smoke);
		height: 4.8em;

		max-width: 1000px;
		margin: 0 auto;
		border-bottom: 1px solid var(--eunry);
	}

	overlay {
		background-color: var(--bokara-grey);
		display: block;
		position: absolute;
		height: 100%;
		width: 100%;
		top: 4.8em;
		z-index: 10;
	}

	options {
		display: none;
	}

	hamburger {
		float: left;
	}

	hamburger > span > i {
		font-size: 2em;
		padding-left: 0.9em;
		padding-top: 0.7em;
	}

	@media (min-width: 800px) {
		hamburger {
			display: none;
		}

		top {
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
	}
</style>
