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
  <button class="menu-close" on:click={handleCloseMenu}>
    <img src="/images/icon-close-menu.svg" alt="Close menu" />
  </button>
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
    justify-content: flex-end;
  }
</style>
