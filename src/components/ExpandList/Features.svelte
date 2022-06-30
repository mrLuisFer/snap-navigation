<script>
  import {slide} from 'svelte/transition';

  let iconCalendar = 'images/icon-calendar.svg';
  let iconTodolist = 'images/icon-todo.svg';
  let iconReminder = 'images/icon-reminders.svg';
  let iconPlanning = 'images/icon-planning.svg';
  let showList = false;

  const items = [
    {icon: iconTodolist, value: 'Todo List'},
    {icon: iconCalendar, value: 'Calendar'},
    {icon: iconReminder, value: 'Reminders'},
    {icon: iconPlanning, value: 'Planning'},
  ];

  const handleToggleList = () => {
    showList = !showList;
  };
</script>

<div>
  <div on:click={handleToggleList}><slot /></div>
  {#if showList}
    {#each items as item}
      <div class="list-container" transition:slide={{duration: '200'}}>
        <img src={item.icon} class="list-img" alt={item.value} />
        <p class="list-text">{item.value}</p>
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

  .list-container img {
    width: 17px;
    height: 17px;
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
