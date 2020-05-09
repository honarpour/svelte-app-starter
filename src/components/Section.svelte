<script>
  import { getContext } from "svelte";

  import Image from "./Image";
  import { getTitle } from "../utils";

  const {
    site: { title: alt },
  } = getContext("context");

  const {
    meta: { title },
    images,
  } = $$props;
</script>

<style>
  section {
    display: block;
    margin: 0 0 calc(var(--gutter) * 2) 0;
    padding: 0;
  }
  section:last-child {
    margin-bottom: 0;
  }

  h1 {
    margin: 0 0 var(--gutter) 0;
    padding: 0;
    font-size: calc(var(--font-size) * 2);
  }
</style>

<section>
  <h1>{getTitle(title)}</h1>
  <div>
    {#each images as src}
      <Image {src} {alt} />
    {/each}
  </div>
</section>
