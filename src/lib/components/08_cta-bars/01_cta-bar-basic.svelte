<script>
  /* Call To Action Bar Basic - supports text, button and ghost button
    - elements wrap at lower rez

    author: Joeri van Ees 
  */ 
</script>

<!-- copy component code from here -->
<!-- Call To Action Bar -->
<div class="cta-bar">
  <div class="cta-bar__container">
    <div class="cta-bar__text">
      <span>You can read the English version of our website</span>
    </div>

    <div class="cta-bar__btns">
      <div class="cta-bar__btn">
        <a href="/comp-sandbox">English website</a>
      </div>
  
      <div class="cta-bar__btn--ghost">
        <a href="/comp-sandbox">Ghost button</a>
      </div>
    </div>
  </div>
</div>



<style lang="scss">

// copy component styling from here  
.cta-bar {
  background: #ededed;
  display: flex;
  justify-content: center;
  width: 100%;

  
  &__container {
    width: 100%;
    max-width: 1480px;
    padding: 10px 40px;

    display: flex;
    justify-self: center;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    @include media-breakpoint-down(lg) {
      flex-direction: column;
    }

    @include media-breakpoint-down(sm) {
      padding: 10px 30px;
    }

    .cta-bar__text {
      flex:1 0 auto;
      padding: 0;
      margin: 0;

      font-size: 1.2rem;

      @include media-breakpoint-down(sm) {
        text-align: center;
      }
    }

    .cta-bar__btns {
      flex:0 0 auto;
      display: flex;
      flex-wrap: wrap;
      flex-direction: row;

      @include media-breakpoint-down(lg) {
        margin-top: 10px;
      }

      @include media-breakpoint-down(sm) {
        justify-content: center;
        flex-direction: column;
      }

      .cta-bar__btn:first-child {
        margin-left: 0;
      }

      .cta-bar__btn {
        display: flex;
        align-items: center;
        padding: 0;
        margin: 0;
        background-color: #00a079;
  
        margin-left: 10px;

        border-radius: 20px;
  
        @include media-breakpoint-down(lg) {
        }

        @include media-breakpoint-down(sm) {
        }

        a {
          display: flex;
          align-items: center;
          justify-content: center;
          
          color: $white;
          font-size: 1.2rem;
          width: 200px;
          height: 40px;
        
          padding: 0;
          margin: 0;
        }
  
        &--ghost {
          display: flex;
          align-items: center;
          margin-left: 10px;
  
          @include media-breakpoint-down(lg) {
          }

          @include media-breakpoint-down(sm) {
            margin-top: 10px;
            margin-left: 0;
          }

          a {
            display: flex;
            align-items: center;
            justify-content: center;
  
            border: 2px solid #00a079;
            border-radius: 20px;
            background-color: transparent;
  
            font-size: 1.2rem;
            width: 200px;
            height: 40px;
  
            color: #00a079;
          }
        }

        &--ghost:hover {

          a {
            border: 2px solid #00a079;
            background-color: #00a079;
            color: $white;
            transition: all 0.1s ease-out;
          }
        }
      }
      .cta-bar__btn:hover {
        background-color: #02ce9f;
        transition: all 0.1s ease-out;
      }
    }
  }
}
</style>