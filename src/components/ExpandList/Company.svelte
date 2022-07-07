<script>
  import {slide} from 'svelte/transition';
  import {clickOutside} from '../../utils/clickOutside';
  import MenuItem from '../Menu/MenuItem.svelte';

  const items = ['History', 'Our Team', 'Blog'];

  export let showList = false;
  const handleToggleList = () => {
    showList = !showList;
  };

  const handleCloseList = () => {
    showList = false;
  };
</script>

<div class="container">
  <div
    on:click={handleToggleList}
    use:clickOutside
    on:click_outside={handleCloseList}
  >
    <MenuItem withExpand clicked={showList}>Company</MenuItem>
  </div>
  {#if showList}
    <div class="list-container">
      {#each items as item}
        <div class="list-item" transition:slide={{duration: '200'}}>
          <p class="list-text">{item}</p>
        </div>
      {/each}
    </div>
  {/if}
</div>

<style></style>
