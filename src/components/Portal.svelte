<script>
  import {onMount, onDestroy} from 'svelte';
  import {slide, fade} from 'svelte/transition';

  export let target = globalThis.document.body;

  let ref;

  onMount(() => {
    if (target) {
      target.appendChild(ref);
    }
  });

  onDestroy(() => {
    setTimeout(() => {
      if (ref.parentNode) {
        ref.parentNode.removeChild(ref);
      }
    });
  });
</script>

<div class="portal" bind:this={ref} transition:slide={{duration: '200'}}>
  <div class="portal-shadow" />
  <slot />
</div>

<style>
  .portal {
    position: absolute;
    top: 0;
    right: 0;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    height: 100vh;
  }

  .portal-shadow {
    background: rgba(0, 0, 0, 0.4);
  }
</style>
