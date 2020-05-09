<script>
  export let src;
  export let alt;

  let rotate = false;

  const toggle = () => {
    rotate = !rotate;
  };
</script>

<style>
  div {
    display: inline-block;
    margin: 0 var(--gutter) var(--gutter) auto;
    vertical-align: top;
  }
  div:last-child {
    margin-bottom: 0;
  }

  img {
    width: 200px;
    height: 200px;
    border: 5px solid var(--color-black);
    transform-origin: center;
    transition: transform 0.3s;
    cursor: pointer;
  }
  img:hover {
    border: 5px dotted var(--color-black);
  }
  img.rotate {
    transform: rotate(45deg) scale(0.6);
  }
</style>

<div>
  <img {src} {alt} on:click={toggle} class:rotate draggable="false" />
</div>
