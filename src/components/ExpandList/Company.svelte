<script>
  import {slide} from 'svelte/transition';

  const items = ['Todo List', 'Todo List', 'Reminders', 'Planning'];

  let showList = false;
  const handleToggleList = () => {
    showList = !showList;
  };
</script>

<div>
  <div on:click={handleToggleList}><slot /></div>
  {#if showList}
    {#each items as item}
      <div class="list-container" transition:slide={{duration: '200'}}>
        <p class="list-text">{item}</p>
      </div>
    {/each}
  {/if}
</div>

<style>
  .list-container {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--medium-gray);
    margin: 1.5rem 0 0 1rem;
  }

  .list-container:hover {
    color: var(--almost-black);
  }

  .list-text {
    margin: 0;
    cursor: default;
    font-size: 0.9rem;
  }
</style>
