<script>
  let audiophile = 'images/client-audiophile.svg';
  let databiz = 'images/client-databiz.svg';
  let maker = 'images/client-maker.svg';
  let meet = 'images/client-meet.svg';

  const companies = [audiophile, databiz, maker, meet];
</script>

<div class="companies-container">
  {#each companies as companyLogo}
    <img src={companyLogo} alt="random" class="companies-logo" />
  {/each}
</div>

<style>
  .companies-container {
    display: flex;
    align-items: center;
    column-gap: 0.5rem;
    justify-content: space-between;
    padding: 0 0.9rem 1rem;
  }

  .companies-logo {
    width: 70px;
    transition: 0.15s ease;
    user-select: none;
  }

  .companies-logo:hover {
    transform: scale(1.1);
  }
</style>
