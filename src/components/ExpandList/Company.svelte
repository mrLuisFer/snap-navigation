<script>
  import {slide} from 'svelte/transition';

  const items = ['History', 'Our Team', 'Blog'];

  let showList = false;
  const handleToggleList = () => {
    showList = !showList;
  };
</script>

<div class="container">
  <div on:click={handleToggleList}><slot /></div>
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
