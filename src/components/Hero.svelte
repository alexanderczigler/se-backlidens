<hero />

<style>
  hero {
    display: block;
    background-attachment: fixed;
    background-color: var(--falu);
    background-image: url("/liza-mobile.jpg");
    background-position: 0 2em;
    background-repeat: no-repeat;
    background-size: 100%;
    margin: 0;
    height: 14em;
    width: 100%;

    -moz-box-shadow: inset 0 0 10px var(--grayscale);
    -webkit-box-shadow: inset 0 0 10px var(--grayscale);
    box-shadow: inset 0px 11px 8px -10px var(--grayscale),
      inset 0px -11px 8px -10px var(--grayscale);
  }

  @media (min-width: 800px) {
    hero {
      background-image: url("/liza.jpg");
      background-position: 0 -30em;
      background-size: cover;
      height: 32em;
    }
  }
</style>
