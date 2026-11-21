<script>
  let { links = [] } = $props();
</script>

<header>
  <a class="logo" href="#top">Conch</a>
  <nav>
    {#each links as link (link.id)}
      <a href={`#${link.id}`}>{link.label}</a>
    {/each}
  </nav>
</header>

<style>
  header {
    position: sticky;
    top: 0;
    z-index: 10;
    height: var(--header-h);
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    padding: 0 24px;
    background: var(--bg);
    border-bottom: 1px solid var(--line);
  }

  .logo {
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  nav {
    display: flex;
    gap: 24px;
  }

  nav a {
    font-size: 0.9rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--muted);
    transition: color 0.15s;
  }

  nav a:hover {
    color: var(--fg);
  }

  @media (max-width: 480px) {
    header {
      padding: 0 16px;
    }

    nav {
      gap: 14px;
    }

    nav a {
      font-size: 0.75rem;
    }
  }
</style>
