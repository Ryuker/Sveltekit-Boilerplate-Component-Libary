<script>
  // component imports
  import BootstrapComponent from "$lib/components/bootstrap-component.svelte";
  import Bs_navbar_01 from "$lib/components/01_navbars/bootstrap/bs_navbar_01.svelte";

  import Flex_footer_4col from "$lib/components/05_footers/flex_footer_4col.svelte";
  import Tiqs_footer_4col from "$lib/components/05_footers/tiqs_footer.svelte";
  import Bs_footer_01 from "$lib/components/05_footers/bootstrap/01_bs_footer.svelte";
  import Bs_foot_4col from "$lib/components/05_footers/bootstrap/02_bs_foot_4col.svelte";
  import Copyright_bar_basic from "$lib/components/06_copyright-bars/01_copyright_bar_basic.svelte";

  import { page } from "$app/stores";
  import currentPageSubTitle from "$lib/stores/my-stores.js";
  import CopyrightBarBasic from "$lib/components/06_copyright-bars/01_copyright_bar_basic.svelte";
  import CopyrightBarMinimal from "$lib/components/06_copyright-bars/02_copyright-bar_minimal.svelte"
  import BsNavbar_01 from "$lib/components/01_navbars/bootstrap/bs_navbar_01.svelte";
  import Basic_Flex_Content_Row from "$lib/components/03_content/01_content-row/basic_flex_content_row.svelte";
  import SlickImageSlider from "$lib/components/07_sliders/01_slick_image_slider.svelte";
  import CTA_Bar_Basic from "$lib/components/08_cta-bars/01_cta-bar-basic.svelte";
  import CTA_Bar_Large from "$lib/components/08_cta-bars/02_cta-bar-basic-and-large.svelte";
  import VideoList from "$lib/components/03_content/08_content_lists/video_lists/01_video_list.svelte";
 


  $: $currentPageSubTitle = "Component Sandbox";



</script>

<svelte:head>
  <title>{$page.routeId}</title>
</svelte:head>

<!-- clear page name -->
<h4>current svelte page - {$page.routeId}</h4> 

<div class="comp-seperator">Bootstrap Navbar 01 - responsive change to hamburger menu</div>
<BsNavbar_01 />

<!-- <Bs_navbar_01 /> -->
<div class="comp-seperator">Flex Footer - 4 columns responsive</div>
<Flex_footer_4col />

<div class="comp-seperator">TIQS Flex footer - 4 Col responsive</div>
<Tiqs_footer_4col />


<div class="comp-seperator">Bootstrap Footer 01 - 4 columns responsive</div>
<Bs_footer_01 />

<div class="comp-seperator">copyright bar basic</div>
<Copyright_bar_basic />

<div class="comp-seperator">copyright bar minimal - justify centered at all rez</div>
<CopyrightBarMinimal />

<!-- <div class="comp-seperator">Bootstrap Footer - 4 Col</div>
<Bs_foot_4col /> -->

<div class="comp-seperator">Basic Flex Content Row - 2 Col</div>
<Basic_Flex_Content_Row />

<!-- <div class="comp-seperator">Slick - Image Slider</div>
<SlickImageSlider /> -->

<div class="comp-seperator">Call To Action Bar Basic - 2 buttons responsive</div>
<CTA_Bar_Basic />

<div class="comp-seperator">Call To Action Bar Large - 1 buttons responsive with bg image + gradient</div>
<CTA_Bar_Large />

<div class="comp-seperator">Video List</div>
<VideoList />



<style lang="scss">

  .comp-seperator {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 30px;
    background-color: azure;
    padding: 10px 0px;
  }
</style>
