<script>
  export let right;
</script>

<block>
  <left aria-current={!right || undefined}>
    {#if right}
      <i class="fa fa-paw" />
    {:else}
      <slot />
    {/if}
  </left>
  <right aria-current={right || undefined}>
    {#if right}
      <slot />
    {:else}
      <i class="fa fa-paw" />
    {/if}
  </right>
</block>

<style>
  left,
  right {
    display: none;
  }

  [aria-current] {
    display: unset;
  }

  @media (min-width: 800px) {
    block {
      display: flex;
      flex-direction: row;
      flex-wrap: nowrap;
      justify-content: center;
      align-items: center;
      align-content: stretch;
      max-width: 1000px;
      margin: 2em auto;
    }

    left {
      display: unset;
      float: left;
      text-align: center;
      vertical-align: middle;
      width: 50%;
    }

    right {
      display: unset;
      float: right;
      text-align: center;
      vertical-align: middle;
      width: 50%;
    }

    i {
      font-size: 6em;
      text-align: center;
    }
  }
</style>
