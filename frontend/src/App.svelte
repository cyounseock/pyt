<script>
  import Router from 'svelte-spa-router'
  import Home from "./rotues/Home.svelte"
  import Detail from "./rotues/Detail.svelte"

  const routes = {
    '/': Home,
    '/detail/:question_id': Detail,
  }
</script>

<Router {routes}/>