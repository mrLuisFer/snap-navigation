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
    border: 1.5px solid var(--almost-black);
    color: var(--medium-gray);
    transition: 0.15s ease;
    margin-top: 0.5rem;
  }

  .menu-login-btn:hover {
    color: var(--almost-black);
  }
</style>
