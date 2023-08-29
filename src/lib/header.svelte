<script>
  import { page } from "$app/stores";
  import currentPageSubTitle from "$lib/stores/my-stores.js";
  import { bind } from "svelte/internal";

  $: curPage = $page.routeId;
</script>

<header>
  <h1>Suprevo Component Library</h1>

  <!-- <h4>Current Page - {curPage != "" ? curPage[0].toUpperCase() + curPage.substring(1) : "Index"}</h4> -->

  <p>{$currentPageSubTitle}</p>
</header>


<style lang="scss">

  header {
    background-color: aquamarine;
    padding: 15px 0px;
    flex-direction: column;
    display: flex;
    justify-content: center;
    

    h1 {
      display: flex;
      justify-content: center;
      margin: 0;
      // color: $my-sass-color;
      color: $my-global-color-var;
    }

    @include my-global-mixin;

    h4{
      flex-direction: row;
      justify-content: center;
      padding: 10px;
      margin: 0;
    }

    p {
      background-color: rgb(107, 184, 71);;
      text-align: center;
      padding: 5px;
      margin: 0;
    }

  }

</style>