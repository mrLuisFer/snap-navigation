<script>
  import Header from './components/Header.svelte';
  import Hero from './components/MainHero.svelte';

  let showMenu = false;
</script>

<main>
  <Header bind:showMenu />
  <Hero />
</main>

<style>
</style>
