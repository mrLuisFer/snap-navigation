<script>
  import MenuItem from './MenuItem.svelte';
  import FeaturesExpandList from '../ExpandList/Features.svelte';
  import CompanyExpandList from '../ExpandList/Company.svelte';
</script>

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
