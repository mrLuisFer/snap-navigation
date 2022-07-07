<script>
  import FeaturesExpandList from '../ExpandList/Features.svelte';
  import CompanyExpandList from '../ExpandList/Company.svelte';
  import MenuItem from './MenuItem.svelte';
</script>

<div class="menu-list">
  <FeaturesExpandList />
  <CompanyExpandList />
  <MenuItem>Careers</MenuItem>
  <MenuItem>About</MenuItem>
</div>

<style>
  .menu-list {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  @media (min-width: 900px) {
    .menu-list {
      display: flex;
      flex-direction: row;
      margin: 0;
    }
  }
</style>
