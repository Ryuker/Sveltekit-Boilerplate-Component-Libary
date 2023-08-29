<script>

</script>

<footer class="foot">
  <div class="foot__content">
    <!-- 4 columns,  -->
    <div class="foot__content__columns">
      <div class="column">
        <ul>
          <li>Kenauweg 14</li>
          <li>Leiden 2331BB</li>
          <li>hello@tiqs.com</li>
          <li>+31 (0) 85 0294999</li>
        </ul>
      </div>
      <div class="column">
        <ul>
          <li><a href="#">Link #1</a></li>
          <li><a href="#">Link #2</a></li>
          <li><a href="#">Link #3</a></li>
          <li><a href="#">Link #4</a></li>
          <li><a href="#">Link #5</a></li>
        </ul>
      </div>
      <div class="column socials">
        <ul>
          <li>
            <a href="https://twitter.com/home">
              <i class="fa-brands fa-twitter"></i>
            </a>
        </li>
          <li>
            <a href="https://www.facebook.com/">
              <i class="fa-brands fa-facebook"></i>
            </a>
          </li>
          <li>
            <a href="https://instagram.com/">
              <i class="fa-brands fa-instagram"></i>
            </a>
          </li>
        </ul>
      </div>
      <div class="column">
        <ul>
          <li><a href="#">Disclaimer</a></li>
          <li><a href="#">Privacy Policy</a></li>
        </ul>
      </div>
    </div>
  </div>
</footer>

<style lang="scss">

.foot {
  // background-color: $white;
  background-color: #957ded;
  // padding: 40px 40px;
  // margin: 0 20px;
  display: block;
  width: 100%;

  @include media-breakpoint-down(md) {
    padding: 40px 0px;
    
  }

  @include media-breakpoint-down(sm) {
    padding: 40px 0px;

  }


  &__content {
    background-color: $white;
    display: block;
    width: 100%;
    max-width: 1240px;
    justify-content: center;
    margin: 0 auto;
    

    @include media-breakpoint-down(sm) {
      // padding: 0 20px;
    }

    &__columns{
      // background-color: red;
      padding: 0 0;
      display: flex;
      justify-content: space-between;
      align-content: flex-start;

      .column{
        // background-color: rgb(151, 151, 199);
        padding: 0 20px;
        width: 100%;
        align-content: flex-start;

        ul {
          padding: 0;
          margin: 0;
          text-decoration: none;
          list-style: none;
          text-align: left;

          li {
            margin: 0;
            padding: 0;
            font-size: 1.0rem;
            color: rgb(138, 136, 136);
            // display: inline;

            a {
              // margin-top: 15px;
              margin-bottom: 20px;
              // background-color: yellow;
              display: block;
              min-width: 120px;
              max-width: 180px;
              text-decoration: none;
              text-transform:capitalize;
              white-space: wrap;
              color: rgb(25, 71, 139);
            }

            a:hover {
              color: rgb(228, 110, 6);
            }
          }
          li:last-child{
            a {
              margin-bottom: 0;
            }
          }
        }

        &.socials {
          // background-color: aqua;
          ul {
            // background-color: aqua;
            display: flex;
            height: 100%;
            li {
              display: inline-flex;
              padding: 0 10px;

              a {
                width: 48px;
                height: 48px;
                min-width: 48px;
                padding-bottom: 0;
                margin-bottom: 0;
                justify-content: center;

                i {
                  padding-top: 5px;
                  font-size: 1.8rem;
                }
              }
            }
          }
        }
        @include media-breakpoint-down(md) {
          width: 50%;
        }

        //nth childe second pakt elke tweede
      }

      .column:first-of-type, .column:last-of-type {
        // background-color: aqua;
        padding: 0;
      }

      @include media-breakpoint-down(md) {
        // background-color: green;
        flex-wrap: wrap;

        .column {
          // background-color: rgb(0, 255, 217);
          display: block;
          width: 50%;
          padding: 0 0 40px;

          ul > li > a {
            max-width: 100%;
          }
        }
      }
      @include media-breakpoint-down(sm) {
        // background-color: green;
        flex-wrap: wrap;

        .column {
          // background-color: rgb(210, 238, 234);
          display: block;
          width: 100%;
          padding: 40px 0;
        }
      }
    }
    
  }

  
}


</style>

