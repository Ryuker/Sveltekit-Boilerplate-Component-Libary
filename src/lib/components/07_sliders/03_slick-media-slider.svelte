<svelte:head>
  <link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
</svelte:head>

<script>
  /* Slick Media Slider 
  - powered by Jquery
  - supports videos and images
  - custom styled dots and navigation

  - based on media slider on vanstooten.nl

    author: Joeri van Ees - 02-08-2022

    how to import jquery: https://www.youtube.com/watch?v=WdVqxZH34R4
   */


   import { onMount } from 'svelte';
   import jQuery from "jquery/dist/jquery";

   onMount(async () => {
    const module = await import('slick-carousel');    // import jquery

    jQuery('.slider').on('click', function() { // test if jquery is working
      console.log("click");
    })

    // fullscreen image slider
    // navigation
    jQuery('.slider-nav-prev').click(function(){
      jQuery('.full-screen-media-slider').slick('slickPrev');
    })

    jQuery('.slider-nav-next').click(function(){
      jQuery('.full-screen-media-slider').slick('slickNext');
    })

    // copy below code into theme
    // expertise slider
    // slider settings
    jQuery('.full-screen-media-slider').slick({
      slidesToShow: 1,
      autoplay: false,
      dots: true,
      arrows: false,
      // prevArrow: true,
      // nextArrow: true,
      slidesToScroll: 1,
      infinite: true,
      fade: true,
      cssEase: 'linear'
    });
    
  });

  </script>

  <!-- full screen image slider -->
<div class="container-fluid">
  <div class="full-screen-media-slider" style="min-height: 100vh;">

    <div>
      <video autoplay muted loop poster="static/placeholders/stock-image.jpeg" class="">
        <source src="https://www.w3schools.com/tags/mov_bbb.mp4" type="video/mp4">
      </video>   
    </div>

    <div>
      <img class="" src="static/placeholders/phone_placeholder_01.png" alt="some header image"/>
    </div>

    <div>
      <img class="" src="static/placeholders/phone_placeholder_02.png" alt="some header image"/>
    </div>
    
    <div>
      <img class="" src="static/placeholders/phone_placeholder_03.png" alt="some header image"/>
    </div>

    <div>
      <img class="" src="static/placeholders/phone_placeholder_04.png" alt="some header image"/>
    </div>
  </div>
</div>

<style lang="scss" global>

.container-fluid {
  position: relative;
  background:  red;
  margin: 0;
  padding: 0;
  height: 100vh;
}


.full-screen-media-slider {
  position: relative;
  width: 100%;
  height: 100vh;
  min-height: 100vh;
  padding: 0;
  margin: 0;

  .bg-img {
    position: absolute;
    top: 0px;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -20;

    object-fit: cover;
  }

  .slick-list .draggable {
    background-color: aqua;
    width: 100%;
    height: 100vh;
  }

  .slick-slide {
    position: relative;
    width: 100%;
    height: 100vh;

    img {
      position: absolute;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    video {
      position: absolute;
      display: block;
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
    }
  }

  .slick-track, .slick-list, .slick-slide {        
    height: 100vh; 
    margin: 0;
  }
  
  .slick-dots {
    position: relative;
    display: block;

    top: -110px;
    z-index: 1;
    width: 100%;
    list-style: none;
    text-align: center;
    padding: 0;

    
    li {
      display: inline-block;
      height: 100%;
      margin: 0 4px;
      padding: 0;

      button {
        background: $white;
        height: 14px;
        width: 14px;
        overflow: hidden;
        border: none;
        outline: none;
        border-radius: 50px;
        line-height: 0;
        font-size: 0.5;
        color: transparent;

        &:hover {
          background-color: $blue;
          color: $blue;
          // outline: 3px solid $blue;
        }
      }

      &.slick-active {
        pointer-events: none;

        button {
            background: $blue;
            color: $blue;
            // outline-offset: 3px;
            // outline: 3px solid $blue;
        }
      }
    }
  }
}

</style>

