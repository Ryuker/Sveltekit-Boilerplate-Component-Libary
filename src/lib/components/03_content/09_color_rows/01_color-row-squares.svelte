<script>
  /* Color Row Squares

  - Row of colors with space between, wraps at mobile rez
  - Divs are colored squares
  - optional label for color below square
  - Uses padding bottom trick in scss


  - based on color row used on customize on vanstooten.nl

    author: Joeri van Ees  10-08-2022
   */
</script>

<div class="row color-row">
  <div class="col-12 colors">
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #114377"></div>
      </div>
      <span>Pantone<br>#1</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #5880bf"></div>
      </div>
      <span>Pantone<br>#2</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #aec3d4"></div>

      </div>
      <span>Pantone<br>#3</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #6f787d"></div>
      </div>
      <span>Pantone<br>#4</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #9a8274"></div>
      </div>
      <span>Pantone<br>#5</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #9a8274"></div>
      </div>
      <span>Pantone<br>#6</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #c1b7a7"></div>
      </div>
      <span>Pantone<br>#7</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #de4e36"></div>
      </div>
      <span>Pantone<br>#8</span>
    </div>
    <div class="col-color">
      <div class="color-box">
        <div class="color" style="background: #e26221"></div>
      </div>
      <span>Pantone<br>#9</span>
    </div>

  </div>
</div>


<style lang="scss">

.color-row {
  margin-bottom: 50px;

  @include media-breakpoint-down(lg) {
    margin-bottom: 30px;
  }

  .colors {
    // background: red;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    .col-color {
      display: flex;
      flex-direction: column;
      width: calc(11.1% - 5px);

      @include media-breakpoint-down(lg){
        flex-wrap: wrap;
        width: calc(25% - 5px);
        margin-bottom: 20px;
      }

      .color-box {
        background: purple;
        width: 100%;
        height: 0;
        position: relative;
        padding-bottom: 100%;

        .color {
          position: absolute;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
        }
      }

      span {
        display: block;
        // background: blue;
        font-size: 1rem;
      }
    }
  }
}

</style>