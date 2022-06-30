<script>
  import MenuItem from './MenuItem.svelte';
  import FeaturesExpandList from '../ExpandList/Features.svelte';
  import CompanyExpandList from '../ExpandList/Company.svelte';

  export let showMenu = false;

  const handleCloseMenu = () => {
    showMenu = false;
  };
</script>

<section class="menu">
  <div class="menu-close" on:click={handleCloseMenu}>
    <img src="/images/icon-close-menu.svg" alt="Close menu" />
  </div>
  <div class="menu-list">
    <FeaturesExpandList>
      <MenuItem withExpand>Features</MenuItem>
    </FeaturesExpandList>
    <CompanyExpandList>
      <MenuItem withExpand>Company</MenuItem>
    </CompanyExpandList>
    <MenuItem>Careers</MenuItem>
    <MenuItem>About</MenuItem>
  </div>
  <div class="menu-login">
    <p>Login</p>
    <button>Register</button>
  </div>
</section>

<style>
  .menu {
    height: 100%;
    background: var(--almost-white);
    padding: 1rem 1rem 10px;
  }

  .menu-close {
    display: flex;
    justify-content: flex-end;
  }

  .menu-list {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }
</style>
