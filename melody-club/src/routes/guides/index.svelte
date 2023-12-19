<script context="module">
  export async function load({ fetch }) {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts')
    const guides = await res.json()

      return {
        props: {
          guides
        }
      }
  
  }
</script>

<script>
  export let guides
</script>

<div class="guides">
  <ul>
    {#each guides as guide}
      <li>
        <a href={`/guides/${guide.id}`}>{guide.title}</a>
      </li>
    {/each}
  </ul>
</div>

<style>
  .guides {
    margin-top: 20px;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  a {
    display: inline-block;
    margin-top: 10px;
    padding: 10px;
    border: 1px dotted rgba(44, 62, 80, 0.2); /* Adjusted border color */
  }
</style>