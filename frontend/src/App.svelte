<script>
  import Router from 'svelte-spa-router'
  import Home from "./rotues/Home.svelte"

  const routes = {
    '/': Home,
  }
</script>

<Router {routes}/>