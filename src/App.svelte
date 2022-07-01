<script>
  import Header from './components/Header.svelte';
  import Hero from './components/MainHero.svelte';
  import MobileMenu from './components/Menu/Menu.svelte';
  import Portal from './components/Portal.svelte';

  let showMenu = false; 
</script>

<main class="main">
  {#if showMenu}
    <Portal>
      <MobileMenu bind:showMenu />
    </Portal>
  {/if}
  <Header bind:showMenu />
  <Hero />
</main>

<style>
  @media (min-width: 900px) {
    .main {
      padding: 0 1.5rem;
    }
  }
</style>
