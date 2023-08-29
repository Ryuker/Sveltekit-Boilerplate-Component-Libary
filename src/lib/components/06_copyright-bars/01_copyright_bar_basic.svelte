<script>
  /* Copyright Bar Basic 
  - 2022 © company name + Privacy policy + Social Icons - Developed by 
  - - desktop: all in one row |  tablet: cb_left on one line + cb_right in next row |  mobile: 3 rows (copyright + privacy policy) - social icons - developed by

  author: Joeri van Ees 
  */
</script>


<div class="copyright-bar">
  <div class="cb__left">
    <span class="copyright">2022 © company name </span>
    <a href="/comp-sandbox">privacy policy</a>
    <div class="social-icons">
      <a href="/comp-sandbox">
        <i class="fa-brands fa-linkedin"></i>
      </a>
      <a href="/comp-sandbox">
        <i class="fa-brands fa-twitter"></i>
      </a>
      <a href="/comp-sandbox">
        <i class="fa-brands fa-facebook"></i>
      </a>
    </div> 
  </div>
  <div class="cb__right">
    <a class="dev-credit" href="https://suprevo.com/">Developed by Suprevo</a>
  </div>
</div>

<style lang="scss">
  .copyright-bar {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    min-height: 100px;
    flex-wrap: wrap;
    
    .cb__left {
      display: flex;
      align-items: center;

      .copyright {
        display: flex;
        padding-right: 30px;
        align-items: center;
        margin-right: 20px;
        flex-wrap: wrap;
        border-right: 1px solid black;
      }

      a {
        text-decoration: none;
      }

      .social-icons{
        padding-left: 20px;
      }

      .social-icon {
        padding: 10px 2px;
        justify-content: center;
        display: inline-block;

        i {
          
        }

        &:hover {
          svg path {
            fill: rgb(157, 156, 156);
          }
        }
      }
    }
    

    .cb__right {
      a {
        display: flex;
        justify-content: start;
        text-decoration: none;
      }

      .dev-credit {
        display: flex;
        align-items:flex-end;
      }

      a {
        text-decoration: none;
      }
    }

    
    // start when screen width = < 768px
    @include media-breakpoint-down(md) {
      flex-wrap: wrap;
      display: block;
      justify-content:space-evenly;

      .cb__left{
        flex-wrap: wrap;
        justify-content: center;
      }

      .cb__right {
        display: flex;
        justify-content: center;
      }

      .copyright {
        justify-content: center;
        align-items: center;
      }

      .social-icons {
        padding: 20px 0;
      }
      .dev-credit {
        padding: 0;
      }
    }

    @include media-breakpoint-down(sm)
    {
      .cb__left {
        .copyright {
        padding-right: 30px
        }

        a {
          padding: 0;
        }
      }
    }
  }
</style>