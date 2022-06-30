<script>
  export let showMenu = false;

  const handleShowMenu = () => {
    showMenu = true;
  };
</script>

<header class="header">
  <a href="/">
    <img src="/images/logo.svg" alt="Snap" />
  </a>
  <button class="menu-btn" on:click={handleShowMenu}>
    <img src="/images/icon-menu.svg" alt="Snap" />
  </button>
</header>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    padding: 1rem 10px 0 10px;
  }

  .menu-btn {
    background: transparent;
    border: none;
    outline: none;
    user-select: none;
  }
</style>
