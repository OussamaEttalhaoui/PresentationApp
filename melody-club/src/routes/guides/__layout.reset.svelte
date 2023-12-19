<script>
  import Title from '$lib/title.svelte'
  import '../../styles/global.css'
</script>

<header>
  <nav>
    <Title title="Melody Club" />
    <div class="links">
      <a href="/">Home</a>
      <a href="/about">About</a>
      <a href="/guides">Guides</a>
    </div>
  </nav> 
</header>
<main>
  <slot></slot>
</main>
<footer>
  <p>© 2023 Melody Hub. All rights reserved.</p>
</footer>

<style>
  header {
    text-align: center;
    background: rgba(236, 240, 241, 0.1); /* Adjusted background color */
  }
  main {
    max-width: 960px;
    margin: 20px auto;
  }
  footer {
    text-align: center;
  }
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #03883f; /* Melody Club's primary color */
    padding: 10px;
  }
  .links {
    display: flex;
    gap: 20px;
  }
  a {
    text-decoration: none;
    color: #ecf0f1; /* Light text color for better contrast */
    font-weight: bold;
    font-size: 16px;
    transition: color 0.3s ease;
  }
  a:hover {
    color: #2c3e50; /* Darker color on hover for better visibility */
  }
</style>