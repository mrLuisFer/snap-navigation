<script>
  import MenuList from './Menu/MenuList.svelte';
  import MenuLogin from './Menu/MenuLogin.svelte';

  export let showMenu = false;
  const handleShowMenu = () => {
    showMenu = true;
  };
</script>

<header class="header">
  <div class="header-nav">
    <a href="/" class="header-nav-logo">
      <img src="/images/logo.svg" alt="Snap" />
    </a>
    <div class="header-list">
      <MenuList />
    </div>
  </div>
  <button class="menu-btn" on:click={handleShowMenu}>
    <img src="/images/icon-menu.svg" alt="Snap" />
  </button>
  <div class="header-login"><MenuLogin /></div>
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

  .header-list {
    display: none;
  }

  .header-login {
    display: none;
  }

  @media (min-width: 900px) {
    .header-list {
      display: block;
    }

    .header-nav {
      display: flex;
      align-items: center;
      gap: 3.5rem;
    }

    .header-nav-logo img {
      margin-top: 0.7rem;
    }

    .menu-btn {
      display: none;
    }

    .header-login {
      display: block;
    }
  }
</style>
