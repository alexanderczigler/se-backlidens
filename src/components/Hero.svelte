<hero />

<style>
  hero {
    display: block;
    background-attachment: fixed;
    background-color: var(--falu);
    background-image: url("/liza-mobile.jpg");
    background-position: 0 -5em;
    background-repeat: no-repeat;
    background-size: 100%;
    margin: 0;
    height: 9em;
    width: 100%;

    -moz-box-shadow: inset 0 0 10px var(--grayscale);
    -webkit-box-shadow: inset 0 0 10px var(--grayscale);
    box-shadow: inset 0px 11px 8px -10px var(--grayscale),
      inset 0px -11px 8px -10px var(--grayscale);
  }

  @media (min-width: 800px) {
    hero {
      background-image: url("/liza.jpg");
      background-position: 0 -12em;
      background-size: cover;
      height: 24em;
    }
  }

  @media (min-width: 1400px) {
    hero {
      background-image: url("/liza.jpg");
      background-position: 0 4em;
      height: 24em;
    }
  }
</style>
