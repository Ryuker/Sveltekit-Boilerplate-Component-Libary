<script>
  import currentPageSubTitle from "$lib/stores/my-stores.js";
  // component imports
  import BootstrapComponent from "$lib/components/bootstrap-component.svelte";
  
  import SingleCard from "$lib/components/07_cards/01_card.svelte";
  import SingleCardWithHeading from "$lib/components/07_cards/02_card-w-heading.svelte";
  import SingleCardWithHeadingAndBTN from "$lib/components/07_cards/03_card-w-heading-btn.svelte";
  import SingleCardWithMedia from "$lib/components/07_cards/04_card-w-media.svelte";
  import SingleCardVaryingSizes from "$lib/components/07_cards/05_card-w-varying-sizes.svelte";
  import SingleCardWithoutBGImage from "$lib/components/07_cards/06_card-without-bg.svelte";
  import IconRow from "$lib/components/03_content/07_icon-row/01_icon-row.svelte";
  import IconRowIconW100 from "$lib/components/03_content/07_icon-row/02_icon-row-responsive_w_100.svelte";
  import IconsStacked from "$lib/components/03_content/07_icon-row/03_icon-row-circle-border.svelte";

  import BasicContactForm from "$lib/components/03_content/02_Forms/02_contact-forms/01_basic-contact-form.svelte";
  import ContactFormWIconAndCaptcha from "$lib/components/03_content/02_Forms/02_contact-forms/02_contact-form-w-icon-captcha.svelte";
  import ContactFormWIconOnTop from "$lib/components/03_content/02_Forms/02_contact-forms/03_contact-form-icon-above.svelte";
  import ContactFormWSplitColInputFields from "$lib/components/03_content/02_Forms/02_contact-forms/04_contact-form-split-col-input-fields.svelte";
  import UserCheckboxTable from "$lib/components/03_content/04_tables/02_table-user-checkbox.svelte";
  import TabMenu from "$lib/components/03_content/05_tab_menus/01_tab-menu.svelte";
  import AccordionMenu from "$lib/components/03_content/05_tab_menus/02_tab-accordion-menu.svelte";
  import TabPlusAccordionMenu from "$lib/components/03_content/05_tab_menus/03_tab-menu_w_accordion.svelte";
  import SlickSliderMultipleElements from "$lib/components/07_sliders/02_slick_slider-multiple-elements.svelte";
  import SlickMediaSlider from "$lib/components/07_sliders/03_slick-media-slider.svelte";
  import NavbarWMobileSupport from "$lib/components/01_navbars/02_navbar_w-mobile-support.svelte"; 
  import HeaderFullScreenSlider from "$lib/components/09_headers/fullscreen/01_header-fullscreen-slider.svelte"; 
  import ColorRowSquares from "$lib/components/03_content/09_color_rows/01_color-row-squares.svelte"; 
  import VanStootenFooter from "$lib/components/05_footers/vanstooten_footer.svelte"; 
  import ContactFormSplitColSimple from "$lib/components/03_content/02_Forms/02_contact-forms/05_contact-form-split-col-simple.svelte"; 
  import QuotationForm from "$lib/components/03_content/02_Forms/01_quotation-forms/01_quotation-form.svelte"; 
  import DivFilter from "$lib/components/03_content/10_filters/01_div-filter.svelte"; 
  import FancyboxGallery from "$lib/components/10_image-grids/01_fancybox-gallery.svelte"; 
  



import { page } from "$app/stores";
import HeaderFullscreenSlider from "$lib/components/09_headers/fullscreen/01_header-fullscreen-slider.svelte";
 


  $: $currentPageSubTitle = "Comp-Builder-Page";
</script>

<svelte:head>
  <title>{$page.routeId}</title>
</svelte:head>

<!-- clear page name -->
<h4>current svelte page - {$page.routeId}</h4> 


<!-- <div class="comp-seperator">Single Card</div>
<SingleCard /> -->

<!-- <div class="comp-seperator">Single Card with heading</div> -->
<!-- <SingleCardWithHeading /> -->

<!-- <div class="comp-seperator">Single Card with heading + btn</div> -->
<!-- <SingleCardWithHeadingAndBTN /> -->

<!-- <div class="comp-seperator">Single Card with media</div> -->
<!-- <SingleCardWithMedia /> -->

<!-- <div class="comp-seperator">Single Card - varying sizes</div> -->
<!-- <SingleCardVaryingSizes /> -->

<!-- <div class="comp-seperator">Single Card - without bg image</div> -->
<!-- <SingleCardWithoutBGImage /> -->

<!-- <div class="comp-seperator">Icon Row - responsive v1</div> -->
<!-- <IconRow /> -->

<!-- <div class="comp-seperator">Icon Row - responsive v2</div> -->
<!-- <IconRowIconW100 /> -->

<!-- <div class="comp-seperator">Icon Row - stacked over circle</div> -->
<!-- <IconsStacked /> -->


<!-- <div class="comp-seperator">Basic Contact Form - Responsive</div>
<BasicContactForm />

<div class="comp-seperator">Contact Form with Icon and Captcha - Responsive</div>
<ContactFormWIconAndCaptcha />

<div class="comp-seperator">Contact Form with Icon on top - Responsive</div>
<ContactFormWIconOnTop />

<div class="comp-seperator">Contact Form with SplitCol Input Fields - Responsive</div>
<ContactFormWSplitColInputFields />

<div class="comp-seperator">Table Standard</div>
<TableStandard />

<div class="comp-seperator">User Checkbox Table</div>
<UserCheckboxTable /> -->

<!-- <div class="comp-seperator">Tab Menu - Responsive</div>
<TabMenu />

<div class="comp-seperator">Accordion Menu </div>
<AccordionMenu />

<div class="comp-seperator">Tab switches to Accordion Menu - Responsive</div>
<TabPlusAccordionMenu /> -->

<!-- <div class="comp-seperator">Slick Slider Multiple Elements - Responsive</div>
<SlickSliderMultipleElements /> -->

<!-- <div class="comp-seperator">Slick Media Slider - Responsive</div>
<SlickMediaSlider /> -->

<!-- <div class="comp-seperator">Slick Media Slider - Responsive</div>
<NavbarWMobileSupport/> -->

<!-- <div class="comp-seperator">Header Full Screen Slider - Responsive</div>
<HeaderFullscreenSlider/> -->

<!-- <div class="comp-seperator">Color Row Squares with label - Responsive</div>
<ColorRowSquares/> -->

<!-- <div class="comp-seperator">VanStooten Footer - Responsive</div>
<VanStootenFooter/> -->

<!-- <div class="comp-seperator">Contact Form Split Col Simple - Responsive</div>
<ContactFormSplitColSimple /> -->

<!-- <div class="comp-seperator">Quotation Form - Responsive</div>
<QuotationForm /> -->

<div class="comp-seperator">Div Filter - Responsive</div>
<DivFilter />

<!-- <div class="comp-seperator">Fancybox Gallery - Responsive</div>
<FancyboxGallery /> -->



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
