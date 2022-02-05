<script>
  export let person = {}

  const { name, title, href, src } = person
</script>

{#if !href}
  <article>
    <img {src} alt="{name} - {title}" />
    <h3>{name}</h3>
    <p>{title}</p>
  </article>
{/if}

{#if href}
  <article>
    <a {href}><img {src} alt="{name} - {title}" /></a>
    <h3><a {href}>{name}</a></h3>
    <p>{title}</p>
  </article>
{/if}

<style>
  article {
    width: 200px;
    margin-bottom: 2rem;
    text-align: center;
  }
  img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    object-position: top;
  }
  h3 {
    margin: 0.5rem 0 !important;
    font-weight: normal;
  }
  p,
  a {
    margin: 0 !important;
    font-weight: normal;
  }
  a:hover {
    text-decoration: none;
  }
</style>
