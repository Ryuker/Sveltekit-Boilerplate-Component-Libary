<svelte:head>
  <title>Welcome Page</title>

  <!-- <script src="jquery/dist/jquery.min.js"></script>
	<script src="slick-caroussel/slick.min.js"></script> -->

</svelte:head>

<script>
  // import { page } from "$app/stores";
  import Layout from "./__layout.svelte";

  import currentPageSubTitle from "$lib/stores/my-stores.js";

  $: $currentPageSubTitle = "My Index Page";
  
</script>

<h1>dynamic title </h1>
<h1> title</h1>
<p>some text in index</p>



<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>
<p>long stuff</p>