<script>
  export let withExpand = false;
  export let listMenuComponent = null;

  let clicked = false;

  const handleClickIcon = () => {
    clicked = !clicked;
  };
</script>

<div class="menu-item" on:click={handleClickIcon}>
  <slot />
  {#if withExpand}
    <img
      src="/images/icon-arrow-down.svg"
      alt="Expand"
      class={clicked ? 'rotateIcon' : 'rotatent'}
    />
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

  .rotateIcon {
    transform: rotate(180deg);
    transition: 0.2s ease;
  }

  .rotatent {
    transform: rotate(0deg);
    transition: 0.2s ease;
  }
</style>
