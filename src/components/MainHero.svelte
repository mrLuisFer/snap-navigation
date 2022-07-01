<script>
  import Companies from './CompaniesLogos.svelte';
</script>

<div class="main-hero">
  <div>
    <img
      src="/images/image-hero-mobile.png"
      alt="Hero mobile"
      class="hero-mobile"
      draggable="false"
    />
  </div>
  <div>
    <section class="hero-content">
      <h1 class="hero-content-title">Make remote work</h1>
      <p class="hero-content-text">
        Get your team in async, no matter your location. Streamline processes,
        create team rituals, and watch productivity soar.
      </p>
    </section>
    <button class="hero-content-btn">Learn more</button>
    <Companies />
  </div>
</div>

<style>
  .hero-mobile {
    width: 100%;
    user-select: none;
  }

  .hero-content {
    text-align: center;
  }

  .hero-content-title {
    font-size: 2rem;
    color: var(--almost-black);
  }

  .hero-content-text {
    color: var(--medium-gray);
    padding: 0 0.5rem;
    line-height: 1.5;
    font-size: 0.9rem;
  }

  .hero-content-btn {
    font-size: 0.9rem;
    background-color: var(--almost-black);
    color: var(--almost-white);
    display: block;
    border-radius: 10px;
    padding: 0.7rem 1rem;
    outline: none;
    border: none;
    margin: 1rem auto 2rem;
    border: 1px solid;
    border-color: transparent;
    transition: 0.15s ease;
  }

  .hero-content-btn:hover {
    background-color: var(--almost-white);
    color: var(--almost-black);
    border-color: var(--almost-black);
  }


  @media (min-width: 900px) {
    .main-hero {
      display: flex;
      flex-direction: row-reverse;
    }
  }
</style>
