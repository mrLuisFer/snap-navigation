<script>
  export let showMenu = false;

  const handleCloseMenu = () => {
    showMenu = false;
  };
</script>

<section class="menu">
  <div class="menu-close" on:click={handleCloseMenu}>
    <img src="/images/icon-close-menu.svg" alt="Close menu" />
  </div>
  <div>
    <p>Features</p>
    <img src="/images/icon-arrow-down.svg" alt="Expand" />
  </div>
</section>

<style>
  .menu {
    position: absolute;
    right: 0;
    height: 100vh;
    width: 50%;
    background: var(--almost-white);
    padding: 1rem 10px 0 10px;
  }

  .menu-close {
    display: flex;
    justify-content: flex-end;
  }
</style>
