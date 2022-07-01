<div class="menu-login">
  <p>Login</p>
  <button class="menu-login-btn">Register</button>
</div>

<style>
  .menu-login {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 2rem;
    color: var(--medium-gray);
    font-size: 0.9rem;
  }

  .menu-login p {
    cursor: default;
    user-select: none;
  }

  .menu-login p:hover {
    color: var(--almost-black);
    transition: 0.1s ease;
  }

  .menu-login-btn {
    width: 100%;
    display: block;
    padding: 0.8rem 0;
    border-radius: 15px;
    border: 2px solid var(--almost-black);
    transition: opacity 0.15s ease;
    margin-top: 0.5rem;
    color: var(--almost-black);
    opacity: 0.5;
    background: transparent;
  }

  .menu-login-btn:hover {
    opacity: 1;
  }

  @media (min-width: 900px) {
    .menu-login {
      display: flex;
      flex-direction: row;
      margin: 0;
      gap: 2rem;
      font-size: 0.85rem;
    }

    .menu-login-btn {
      padding: 0.6rem 1rem;
      border-radius: 13px;
    }
  }
</style>
