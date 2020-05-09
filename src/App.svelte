<script>
  import { setContext } from "svelte";

  import Header from "./components/Header";
  import Main from "./components/Main";
  import Footer from "./components/Footer";

  export let context;
  setContext("context", context);
</script>

<Header siteTitle={context.site.title} />
<Main />
<Footer />
