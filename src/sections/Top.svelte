<script>
  import Logo from "../components/Logo.svelte";
  import Nav from "../components/Nav.svelte";

  export let segment;

  let overlay = false;
  const toggleMenu = () => {
    overlay = !overlay;
  };
</script>

{#if overlay}
  <overlay>
    <Nav {segment} {toggleMenu} />
  </overlay>
{/if}

<top>
  <Logo />

  <hamburger>
    <span>
      <i class="fa fa-bars" on:click={toggleMenu} />
    </span>
  </hamburger>

  <options>
    <Nav {segment} />
  </options>
</top>

<style>
  top {
    display: block;
    text-transform: uppercase;
    background-color: var(--lotion);
    height: 4.8em;
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
