<script>
  /* VanStooten Footer
  - 3 columns
  - contact/socials - button - logo 

    author: Joeri van Ees  10-08-2022
   */

</script>

<footer>
  <!-- 3 columns  -->
  <div class="columns">

    <div class="column mb-5">
      <ul>
        <li>
          <strong>E</strong>
          <a href="mailto:info@vanstooten.nl">info@vanstooten.nl</a>
        </li>
        <li>
          <strong>T</strong>
          <a href="tel:+31(0)10 123 456 89">+31(0)10 123 456 89</a>
        </li>
        <li class="social-icons">
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <!-- <a href="#"><i class="fa-brands fa-facebook"></i>
          <a href="#"><i class="fa-brands fa-youtube"></i></a> -->
        </li>
      </ul>
    </div>

    <div class="column mb-5">
      <a class="button button--icon">Neem contact op<i class="fas fa-paper-plane"></i></a>
    </div>

    <div class="column mb-5">
      <a href="#" class="logo">
        <img src="../../../../static/placeholders/brand_placeholder.svg" alt="brand">
      </a>
    </div> 
  </div>
</footer>


<style lang="scss" global>

.columns {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
    width: 100%;
    padding: 30px 0 0;

    @include media-breakpoint-down(lg) {
      flex-wrap: wrap;
      justify-content: center;
    }

    @include media-breakpoint-down(sm) {
      flex-wrap: wrap;
      justify-content: center;
    }

    .column {
      display: flex;
      width: 25%;
      padding: 0;
      margin: 0;
      font-size: 1rem;

      @include media-breakpoint-down(lg) {
        justify-content: center;
      }

      @include media-breakpoint-down(md) {
        width: 100%;
        justify-content: flex-start;
      }

      &:nth-child(2) {
        width: 50%; 
        display: flex;
        align-items: center;
        justify-content: center;
        @include media-breakpoint-down(md) {
          width: 100%;
          justify-content: flex-start;
        }
      }

      &:nth-child(3) {
        justify-content: flex-end;
        @include media-breakpoint-down(md) {
          width: 100%;
          justify-content: flex-start;
        }
      }

      a, a:hover {
        color: $white;
      }

      ul {
        li {
          font-size: 0.95rem;
          margin-bottom: 5px;
          strong {
            color: $white;
            display: inline-block;
            width: 24px;
          }
          a {
            color: $white;
          }
          &.social-icons {
            display: flex;
            margin-top: 10px;
            margin-left: -10px;
            a {
              display: flex;
              height: 48px;
              width: 48px;
              justify-content: center;
              align-items: center;
              font-size: 1.7rem;
            }
          }
        }
      }

      .logo {
       display: flex;
      //  justify-content: flex-end;

      //   @include media-breakpoint-down(lg) {
      //     justify-content: center;
      //   }

      //   @include media-breakpoint-down(sm) {
      //     justify-content: center;
      //   }
      
        img {
          width: 200px;
          object-fit: fill;
          filter:  brightness(0) invert(1);
        } 
      }

    }
  }
</style>