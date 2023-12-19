<script>
  import Title from '$lib/title.svelte'
  import '../styles/global.css'
</script>

<header>
  <Title title="Melody Club" />
</header>
<main>
  <slot></slot>
</main>
<footer>
  <p>© 2023 Melody Hub. All rights reserved.</p>
</footer>

<style>
  header {
    display: flex;
    justify-content: center;
    background-color: #03883f;
    color: #ecf0f1;
    padding: 10px;
  }
  main {
    max-width: 960px;
    margin: 20px auto;
    padding: 20px;
    background-color: #ecf0f1;
    border-radius: 8px;
    color: #2c3e50;
  }
  footer {
    text-align: center;
    padding: 10px;
    color: #ecf0f1;
  }
</style>