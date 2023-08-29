<script>
  import BootstrapComponent from "$lib/components/bootstrap-component.svelte";
  import { page } from "$app/stores";
  import currentPageSubTitle from "$lib/stores/my-stores.js";

  $: $currentPageSubTitle = "My bootstrap test page subtitle";

</script>

<svelte:head>
  <title>{$page.routeId}</title>
</svelte:head>

<!-- clear page name -->
<h4>current svelte page - {$page.routeId}</h4> 


<BootstrapComponent />