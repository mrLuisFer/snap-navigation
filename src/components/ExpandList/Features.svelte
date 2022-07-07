<script>
  import {slide} from 'svelte/transition';
  import {clickOutside} from '../../utils/clickOutside';
  import MenuItem from '../Menu/MenuItem.svelte';

  let iconCalendar = 'images/icon-calendar.svg';
  let iconTodolist = 'images/icon-todo.svg';
  let iconReminder = 'images/icon-reminders.svg';
  let iconPlanning = 'images/icon-planning.svg';

  export let showList = false
  const items = [
    {icon: iconTodolist, value: 'Todo List'},
    {icon: iconCalendar, value: 'Calendar'},
    {icon: iconReminder, value: 'Reminders'},
    {icon: iconPlanning, value: 'Planning'},
  ];

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
    <MenuItem withExpand clicked={showList}>Features</MenuItem>
  </div>
  {#if showList}
    <div class="list-container">
      {#each items as item}
        <div class="list-item" transition:slide={{duration: '200'}}>
          <img src={item.icon} class="list-img" alt={item.value} />
          <p class="list-text">{item.value}</p>
        </div>
      {/each}
    </div>
  {/if}
</div>

<style global>
  :global(.list-item) {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--medium-gray);
    margin: 1.5rem 0 0 1rem;
  }

  .list-item img {
    width: 17px;
    height: 17px;
  }

  :global(.list-item:hover) {
    color: var(--almost-black);
  }

  :global(.list-text) {
    margin: 0;
    cursor: default;
    font-size: 0.9rem;
  }

  @media (min-width: 900px) {
    :global(.container) {
      position: relative;
    }

    :global(.list-container) {
      position: absolute;
      background-color: #fff;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
      border-radius: 15px;
      top: 30px;
      right: 0;
      padding: 0 1rem;
      min-width: 80px;
    }

    :global(.list-item) {
      display: flex;
      align-items: center;
      gap: 0.8rem;
      margin: 1rem 0;
    }
  }
</style>
