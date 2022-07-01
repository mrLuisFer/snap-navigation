<script>
  import Companies from './CompaniesLogos.svelte';
</script>

<div class="main-hero">
  <div class="main-hero-img">
    <img
      src="/images/image-hero-mobile.png"
      alt="Hero mobile"
      class="hero-mobile"
      draggable="false"
    />
    <img
      src="/images/image-hero-desktop.png"
      alt="Hero mobile"
      class="hero-desktop"
      draggable="false"
    />
  </div>
  <div class="hero-content-container">
    <section class="hero-content">
      <h1 class="hero-content-title">Make <span>remote work</span></h1>
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

  .hero-desktop {
    display: none;
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
    margin: 2rem auto 4rem;
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
      padding: 2.5rem 6rem 0;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-auto-flow: column;
      gap: 5rem;
    }

    .main-hero-img {
      grid-column: 2;
    }

    .hero-content-container {
      grid-column: 1;
    }

    .hero-content {
      text-align: left;
    }

    .hero-content-title {
      font-size: 4rem;
      margin-bottom: 4rem;
    }

    .hero-content-title span {
      display: block;
    }

    .hero-content-text {
      max-width: 400px;
      line-height: 1.8;
    }

    .hero-content-btn {
      margin: 5rem 0 7.5rem;
    }

    .hero-mobile {
      display: none;
    }

    .hero-desktop {
      display: block;
      max-width: 500px;
    }
  }
</style>
