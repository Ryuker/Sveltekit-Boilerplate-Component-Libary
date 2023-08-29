<script>
  /* Flex Footer - 4 columns responsive
  - 4 columns each with a ul list
  - - desktop: 4 col , tablet: 2 col, mobile: 1 col

  author: Joeri van Ees 
  */
</script>

<footer class="foot">
  <div class="foot__content">
    <!-- 4 columns,  -->
    <div class="foot__content__columns">
      <div class="foot__content__columns__column">
        <h4>Heading 1</h4>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="foot__content__columns__column">
        <h4>Heading 2</h4>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="foot__content__columns__column">
        <h4>Heading 3</h4>
        <ul>
          <li><a href="/comp-sandbox">Link #1 this is very long link isn't it</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="foot__content__columns__column">
        <h4>Heading 4</h4>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
    </div>
  </div>
</footer>


<style lang="scss">
  .foot {
    background-color: rgb(149, 125, 237);

    &__content {
      display: flex;
      justify-content: center;
      flex-direction: column;
      padding: 0 20px;

      &__columns{
        background-color: red;
        display: flex;
        justify-content: space-evenly;

        h4 {
          background-color: rgb(189, 189, 222);

        }

        &__column{
          background-color: rgb(151, 151, 199);

          ul {
            padding: 0;
            text-decoration: none;
            list-style: none;
            text-align: left;

            a {
              margin-top: 15px;
              background-color: yellow;
              display: block;
              min-width: 180px;
              max-width: 180px;
              text-decoration: none;
              white-space: wrap;
            }
          }

        }

        @include media-breakpoint-down(md) {
          background-color: green;
          flex-wrap: wrap;

          &__column{
            background-color: rgb(0, 255, 217);
            display: block;
            width: 50%;

            ul > li > a {
              max-width: 100%;
            }
          }
        }
        @include media-breakpoint-down(sm) {
          background-color: green;
          flex-wrap: wrap;

          &__column{
            background-color: rgb(210, 238, 234);
            display: block;
            width: 100%;
          }
        }
      }
    }
  }


</style>



