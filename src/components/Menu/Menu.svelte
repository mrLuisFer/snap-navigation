<script>
  import MenuLogin from './MenuLogin.svelte';
  import MenuList from './MenuList.svelte';

  export let showMenu = false;

  const handleCloseMenu = () => {
    showMenu = false;
  };

  $: document.body.style.overflowY = showMenu ? 'hidden' : 'auto';
</script>

<section class="menu">
  <div class="menu-close-container">
    <button class="menu-close" on:click={handleCloseMenu}>
      <img src="/images/icon-close-menu.svg" alt="Close menu" />
    </button>
  </div>
  <MenuList />
  <MenuLogin />
</section>

<style>
  .menu {
    height: 100%;
    background: var(--almost-white);
    padding: 1rem 1rem 10px;
  }

  .menu-close {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid transparent;
    background: var(--almost-white);
    transition: 0.2s ease;
    border-radius: 10px;
  }

  .menu-close:hover {
    border-color: var(--almost-black);
  }

  .menu-close-container {
    display: flex;
    justify-content: flex-end;
  }
</style>
