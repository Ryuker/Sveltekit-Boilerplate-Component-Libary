<script>
  /* Basic Flex Content Row - supports 2 columns
    - each 50% of wrapper width
    - supports image left, or image right
    - image can be 
    - use reverse-mobile class on section to reverse order of columns on mobile width
    - supports video and tablet-slider ( * was made for TIQS so might not be reusable)

  */ 
</script>


<section class="content-row bg-purple">
  <div class="content-row__wrapper">
    <div class="content-columns">
      <div class="text-col">
        <div class="text-col_inner">
          <h1>Hoe tiqs met een QR code ervoor zorgt dat je business groeit</h1>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed sapien enim, facilisis non rhoncus sed, tincidunt a augue. Donec euismod imperdiet diam convallis pellentesque. 
          </p>
          <div class="btns">
            <a class="button" href="/comp-sandbox">vraag naar de voorwaarden</a>
            <a class="button button--ghost" href="/">beetje tekst</a>
          </div>
        </div>
      </div>
      <div class="image-col regular">
        <img src="static/placeholders/stock-image.jpeg" alt="stock photo"/>
      </div>
    </div>
  </div>
</section>


<style lang="scss">
// Global colors
$black: #0c0c0c;
$white: #ffffff;

// Project colors
$light-blue: #95C8D8;
$blue: #00A0D3;
$navy-blue: #203C87;
$orange: #CE6925;
$dark-blue: #002B45;
$light-green: #4eaf98;
$yellow: #ffbc00;
$red: #E5393D;

// more colors
$purple: #B47EDE;
$pink: #DA3978;
$green: #72B19F;

.button {
  display: inline-block;
  background-color: $light-green;
  color: $white;
  padding: 16px 22px;
  font-weight: 600;
  font-size:1rem;
  text-transform: uppercase;
  text-decoration: none;
  margin-bottom: 10px;
  margin-right: 10px;
  i {
    padding-left: 40px;
  }

  &:hover {
    text-decoration: none;
    color: $white;
    background: lighten($blue, 4);
    transition: 0.5s ease;
  }

  &--ghost {
    display: inline-block;
    border: 2px solid $white;
    background-color: transparent;
    box-shadow: none;
    color: $white;
    padding: 14px 20px;
    &:hover {
      background: $white;
      color: $orange;
      transition: 0.2s ease;
    }
  }
}

@include media-breakpoint-down(sm) {
  .button, .button--ghost {
    width: 100%;
    text-align: center;
  }
  
}


.content-row {
  background-color: $yellow;
  display: block;
  // width: 100%;
  color: $white;
  padding: 120px 0;

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
        // height: 100%;
        width: 50%;

        &.regular {
          padding: 0 40px;
          @include media-breakpoint-down(md) {
            width: 100%;
            padding: 0;
            margin-bottom: 40px;
          }
        }

        &.smartphone {
          bottom: -180px;
          margin-top: -160px;

          @include media-breakpoint-down(md) {
            bottom: 0;
            margin-top: 40px;
            width: 100%;
          }

          span {
            position: absolute;
            width: 307px;
            height: 97%;
            margin: 0 auto;
            left: 0;
            right: 0;
            border-radius: 45px;
            overflow: hidden;

            video {
              position: absolute;
              width: 100%;
              object-fit: cover;
              height: 100%;
            }
          }

          img {
            align-self: center;
            justify-self: center;
            width: 330px;
          }
        }

        &.tablet {
          span {
            position: absolute;
            width: 310px;
            height: 82%;
            margin: 0 auto;
            top: -44px;
            left: 0;
            right: -57px;
            border-radius: 5px;
            overflow: hidden;

            @include media-breakpoint-down(md) {
              right: 8px;
              top: 14px;
              width: 274px;
            }

            .tablet--slider {
              height: 100%;

              .slick-list,
              .slick-track {
                height: 100%;
                position: relative;

                .slick-slide {
                  position: relative;
                }
              }

              img {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                object-fit: cover;
              }
            }

          }

          &>img {
            align-self: center;
            justify-self: center;
            width: 400px;
            margin-top: -60px;
            padding-bottom: 60px;

            @include media-breakpoint-down(md) {
              margin-top: 0;
              padding-bottom: 0;
              margin-left: -60px;
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

    // @include media-breakpoint-down (lg) {
    //   padding: 40px 80px;
    // }

    // @include media-breakpoint-down(md) {
    //   padding: 30px 40px;
    //   width: 100%;
    // }

    // @include media-breakpoint-down(md) {
    //   padding: 30px 30px;
    //   width: 100%;
    // }

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

// .content-row:first-of-type {
//   margin-top: 98px;
// }

.content-row {
  &.bg-orange {
    background-color: $orange;

    .button:not(.button--ghost) {
      background: $light-green;

      &:hover {
        background: $navy-blue;
      }
    }
  }

  &.bg-blue {
    background-color: $light-blue;

    .button:not(.button--ghost) {
      background: $orange;

      &:hover {
        background: $navy-blue;
      }
    }
  }

  &.bg-yellow {
    .text-col {

      h1,
      .h1,
      p {
        color: $black;
      }
    }

    .button:not(.button--ghost) {
      background: $navy-blue;

      &:hover {
        background: $orange;
      }
    }

    .button--ghost {
      background: $white;
      color: $orange;

      &:hover {
        color: $black;
      }
    }
  }

  &.bg-red {
    background: $red;

    .button:not(.button--ghost) {
      background: $light-green;

      &:hover {
        background: $navy-blue;
      }
    }

    .button--ghost {
      color: $white;

      &:hover {
        color: $red;
      }
    }
  }

  &.bg-purple {
    background: $purple;

    .button:not(.button--ghost) {
      background: $pink;

      &:hover {
        background: $navy-blue;
      }
    }

    .button--ghost {
      color: $white;

      &:hover {
        color: $purple;
      }
    }
  }

  &.bg-green {
    background: $green;

    .button:not(.button--ghost) {
      background: $pink;

      &:hover {
        background: $navy-blue;
      }
    }

    .button--ghost {
      color: $white;

      &:hover {
        color: $green;
      }
    }
  }
}
</style>