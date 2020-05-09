<script>
  import { getContext } from "svelte";

  import Section from "./Section";

  const {
    site: { desc: description },
    data,
  } = getContext("context");
</script>

<style>
  main {
    display: block;
    margin: 0;
    padding: var(--gutter);
    min-height: 100vh;
  }

  p {
    margin: 0 0 calc(var(--gutter) * 2) 0;
    padding: 0;
  }
</style>

<main>
  <p>{description}</p>

  {#each data as dataItem}
    <Section {...dataItem} />
  {/each}
</main>
