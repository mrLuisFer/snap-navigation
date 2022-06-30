<script>
  export let withExpand = false;
  export let listMenuComponent = null;
</script>

<div class="menu-item">
  <slot />
  {#if withExpand}
    <img src="/images/icon-arrow-down.svg" alt="Expand" />
  {/if}
  <svelte:component this={listMenuComponent} />
</div>

<style>
  .menu-item {
    display: flex;
    align-items: center;
    column-gap: 1rem;
    color: var(--medium-gray);
    font-size: 0.9rem;
    user-select: none;
    transition: 0.15s ease;
  }

  .menu-item:hover {
    color: var(--almost-black);
  }
</style>
