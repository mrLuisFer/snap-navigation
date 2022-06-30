<script>
  import Header from './components/Header.svelte';
  import Hero from './components/MainHero.svelte';
  import Companies from './components/CompaniesLogos.svelte';
  import MobileMenu from './components/MobileMenu/Menu.svelte';
  import Portal from './components/Portal.svelte';

  let showMenu = false; 
</script>

<main>
  {#if showMenu}
    <Portal>
      <MobileMenu bind:showMenu />
    </Portal>
  {/if}
  <Header bind:showMenu />
  <Hero />
  <Companies />
</main>

<style>
</style>
