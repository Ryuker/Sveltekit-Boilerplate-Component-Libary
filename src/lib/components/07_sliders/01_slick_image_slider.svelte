<svelte:head>
  <!-- <script src="static/js/jquery-3.5.1.min.js"></script> -->

  <link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/> -->
  <link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick-theme.css"/>

  

</svelte:head>

<script>
  /* Basic Image Slider 
  - centered in the div
  - powered by Jquery
  - supports images of same width, breaks when width differs too much

  - based on image slider used in Tiqs website.

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
    //jQuery(document).ready(function () { 
    jQuery('.img--slider').slick( {
        infinite: true,
        autoplay: false,
        autoplaySpeed: 1000,
        dots: true,
        speed: 1000,
        slidesToShow: 1,
        slidesToScroll: 1,
        arrows: false,
      });

    jQuery('.img--slider .slick-dots').insertAfter(jQuery('.image-col.slider .img--slider'));
  }); 
  

</script>


<div class="content-row reverse-mobile">
  <div class="content-row__wrapper">
    <div class="content-columns">
      <div class="image-col slider">
        <div class="img--slider">
          <div><img src="static/placeholders/phone_placeholder_01.png" alt=""></div>
          <div><img src="static/placeholders/phone_placeholder_02.png" alt=""></div>
          <div><img src="static/placeholders/phone_placeholder_04.png" alt=""></div>
        </div>
      </div>
      <div class="text-col">
        <div class="text-col__inner">
          <h2 class="h1">Some header text</h2>
          <p>Duis feugiat turpis eu nibh finibus dictum. Vestibulum at nisl quis nulla consequat elementum. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Ut blandit libero risus, dapibus dictum neque auctor porta. Pellentesque dignissim maximus imperdiet.
          </p>
        </div>
        
      </div> 
      
    </div>
  </div>
</div>

<style lang="scss">

// @use "../scss/vendors/slick/slick-theme.scss";
// @use "../scss/vendors/slick/slick.scss";

.content-row {
  background-color: $yellow;
  display: block;
  width: 100%;
  color: $white;
  padding: 80px 0;

  @include media-breakpoint-down(md) {
    padding: 60px 30px;
  }

  &__wrapper {
    display: block;
    width: 100%;
    max-width: 1320px;
    margin: 0 auto;

    .content-columns {
      width: 100%;
      display: flex;
      flex-direction: row;

      @include media-breakpoint-down(md) {
        flex-direction: column;
        width: 100%;
      }

      &>.image-col {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-self: center;
        align-items: center;
        // height: 100%;
        width: 50%;

        &.slider {
          // background-color: aqua;
          padding: 0;
          margin: 0;

          @include media-breakpoint-down(md) {
            width: 100%;
            padding-bottom: 50px;
          } 

          @include media-breakpoint-down(sm) {
            width: 100%;
            padding-bottom: 70px;
          } 

          .img--slider {
            // background-color: aquamarine;
            width: 100%;
            padding: 0;
            margin: 0;

            img {
              align-self: center;
              justify-self: center;
              max-height: 600px;
              // margin-top: 40px;
              // padding-bottom: 40px;
              margin: 40px auto 0 auto;
             
  
              @include media-breakpoint-down(md) {
                margin: 40px auto 0 auto;
                // margin-left: -60px;
                max-height: 400px;
              }            
            }
          }

          .slick-dots {
            li {
              margin: 0;
              button {
                font-size: 48px;
                &:before {
                  font-size: 48px;
                  color: black;
                }
              }
            }
          }
        }
      }

      

      .text-col {
        width: 50%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-self: center;
        padding: 0 40px;

        @include media-breakpoint-down(md) {
          width: 100%;
          margin-bottom: 40px;
          padding: 0;
        }

        a {
          display: inline-block;
        }

        p {
          display: block;
          width: 100%;
          color: $white;
          font-size: 1.1rem;
          flex: 1;
          margin-bottom: 1em;
        }

        h1,
        .h1 {
          padding-bottom: 10px;
          text-transform: uppercase;
          font-family: 'Campton Book', sans-serif !important;
          font-size: 2rem;
          padding-bottom: 10px;

          @include media-breakpoint-down(md) {
            font-size: 1.7rem;
          }
        }

        .btns {
          display: flex;
          flex-wrap: wrap;
          margin-top: 30px;
        }

        &.align-top {
          align-self: flex-start;
        }

      }
    }
  }

  &.reverse-mobile {
    @include media-breakpoint-down(md) {
      .content-row__wrapper {
        .content-columns {
          flex-direction: column-reverse;
        }
      }
    }
  }
}
</style>