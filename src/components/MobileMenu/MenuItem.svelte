<script>
  export let withExpand = false;
</script>

<div class="menu-item">
  <slot />
  {#if withExpand}
    <img src="/images/icon-arrow-down.svg" alt="Expand" />
  {/if}
</div>

<style>
  .menu-item {
    display: flex;
    align-items: center;
    column-gap: 1rem;
    color: var(--medium-gray);
    font-size: 0.9rem;
  }
</style>
