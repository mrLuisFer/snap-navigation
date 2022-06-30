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

<div class="portal" bind:this={ref}>
  <div class="portal-shadow" transition:fade={{duration: '150'}} />
  <div transition:slide={{duration: '200'}}>
    <slot />
  </div>
</div>

<style>
  .portal {
    position: absolute;
    top: 0;
    right: 0;
    width: 100%;
    display: grid;
    grid-template-columns: 120px 1fr;
    height: 100vh;
  }

  .portal-shadow {
    background: rgba(0, 0, 0, 0.4);
  }

</style>
