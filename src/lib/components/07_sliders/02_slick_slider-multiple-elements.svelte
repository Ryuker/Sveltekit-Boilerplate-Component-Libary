<svelte:head>
  <link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
  <link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick-theme.css"/>
</svelte:head>

<script>
  /* Slick Slider Multiple Elements - uses Bootstrap
  - centered in the div
  - powered by Jquery
  - supports images of same width, breaks when width differs too much?

  - based on expertises slider on mavotrans.nl

    author: Joeri van Ees - 19-04-2022

    how to import jquery: https://www.youtube.com/watch?v=WdVqxZH34R4
   */

  import { onMount } from 'svelte';
  import jQuery from "jquery/dist/jquery";

  onMount(async () => {
    const module = await import('slick-carousel');    // import jquery

    jQuery('.slider').on('click', function() { // test if jquery is working
      console.log("click");
    });

    // copy below code into theme
    // expertise slider
    jQuery('.expertises__slider').slick({
      slidesToShow: 5,
      autoplay: false,
      dots: true,
      arrows: true,
      // prevArrow: true,
      // nextArrow: true,
      slidesToScroll: 1,
      infinite: true,
      responsive: [
        {
          breakpoint: 1260,
          settings: {
            slidesToShow: 4,
            slidesToScroll: 1,
            infinite: true,
          }
        },
        {
          breakpoint: 1024,
          settings: {
            slidesToShow: 3,
            slidesToScroll: 1,
            infinite: true,
          }
        },
        {
          breakpoint: 768,
          settings: {
            slidesToShow: 2,
            slidesToScroll: 1,
            infinite: true,
            arrows: false,
          }
        },
        {
          breakpoint: 480,
          settings: {
            slidesToShow: 1,
            slidesToScroll: 1,
            infinite: true,
            arrows: false,
          }
        },
      ]
    });
  });

</script>

<h1>Slick Slider Multiple Elements Component</h1>

<section class="container-fluid my-5 expertises">
  <div class="container" >
    <div class="row" >
      <div class="col-12" >
        <h2 class="text-center mb-5">Onze expertises</h2>
      </div>
    </div>
    <div class="row expertises__slider">
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
      <a href="https://mavotrans.nl/expertise-bouwakoestiek" class="col-12 col-sm-6 col-md-4 col-lg">
        <div class="expertise--blok cut-corner mb-3">
          <span>Bouwakoestiek</span> 
          <img src="static/placeholders/luchtdichtbouwen.jpg" data-original="static/placeholders/luchtdichtbouwen.jpg" alt="" class="img-fill loaded">
        </div>
      </a> 
    </div> 
   </div>
</section>

<style lang="scss">

.expertises {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.expertises__slider {
  display: flex;
  justify-content: space-around;
  max-width: 800px;
}

.expertises__slider .slick-arrow {
  &.slick-disabled {
    opacity: 0.25;
  }

  &.slick-prev {
    left: -20px;
    @include media-breakpoint-down(sm) {
      left: 10px;
    }
    &:before {
      content: '\f053';
      font-family: 'Font Awesome 5 Pro';
      opacity: 1;
      font-weight: 700;
      margin-left: -2px;
      color: $primary;
      font-size: 1.4rem;
    }
  }

  &.slick-next {
    right: -20px;
    @include media-breakpoint-down(sm) {
      right: 10px;
    }
    &:before {
      content: '\f054';
      font-family: 'Font Awesome 5 Pro';
      opacity: 1;
      font-weight: 700;
      margin-right: -2px;
      color: $primary;
      font-size: 1.4rem;
    }
  }
}

</style>