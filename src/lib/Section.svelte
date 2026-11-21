<script>
  let { id, title, children } = $props();
</script>

<section {id}>
  <h2>{title}</h2>
  {@render children?.()}
</section>

<style>
  section {
    min-height: calc(100svh - var(--header-h));
    padding: 48px 24px;
    border-bottom: 1px solid var(--line);
    /* Keep the heading clear of the sticky header when jumping via nav links. */
    scroll-margin-top: var(--header-h);
  }

  h2 {
    font-size: 2rem;
    text-transform: uppercase;
    letter-spacing: 0.06em;
  }

  @media (max-width: 480px) {
    section {
      padding: 32px 16px;
    }
  }
</style>
