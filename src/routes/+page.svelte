<script>
  import Header from "../lib/components/Header.svelte";
	import Landing from "../lib/components/Landing.svelte";
	import ToDo from "../lib/components/ToDo.svelte";
	import Weddings from "../lib/components/Weddings.svelte";
</script>

<Header />

<main>
  <Landing />
  <ToDo />
  <Weddings />
</main>

<style>
  main {
    height: 100vh;
    overflow-y: scroll;
    scroll-snap-type: y mandatory;
  }

  :global(article) {
    scroll-snap-align: start;
  }
</style>