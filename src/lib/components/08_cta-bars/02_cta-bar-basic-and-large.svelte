<script>
  /* Call To Action Bar Large - supports text, button and ghost button (ghost not supported in large extension)
    - elements wrap at lower rez
    - use --large to use large version
    - large version support image with a gradient

    author: Joeri van Ees 
  */ 
</script>

<!-- copy component code from here -->
<!-- Call To Action Bar Large version, supports bg image -->
<div class="cta-bar cta-bar--large">
  <div class="cta-bar__container">
    <img src="./static/placeholders/stock-image.jpeg"/>
    <div class="cta-bar__text">
      <span>You can read the English version of our website</span>
    </div>

    <div class="cta-bar__btns">
      <div class="cta-bar__btn">
        <a href="/comp-sandbox">English website</a>
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

  // Large extension to support image in background with gradient, more padding, larger font etc
  // - does not support Ghost button !
  &--large {
    background: transparent;
    margin-top: 20px;
    width: 100%;

    // padding: 0px 40px;

    @include media-breakpoint-down(sm) {
      padding: 0;
    }
    
    .cta-bar__container {   
      position: relative;
      overflow: hidden;
      border-radius: 20px;
      padding: 50px 40px 50px 40px;
      margin: 0;

      @include media-breakpoint-down(xl) {
        flex-direction: column;
        padding-top: 0;
      }

      @include media-breakpoint-down(sm) {
        padding: 50px 10px 50px 10px;
        border-radius: 0px;
      }

      img { 
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        object-fit: cover;
        z-index: 2;
        position: absolute;
        border-radius: 20px;
        opacity: 1.0;
        padding: 0;
        margin: 0;

        @include media-breakpoint-down (sm) {
          border-radius: 0px;
        }
      }

      .cta-bar__text {
        font-size: 2.0rem;
        color: $white;
        padding-right: 0px;
        z-index: 99;

        @include media-breakpoint-down(xl) {
          text-align: center;
          padding-top: 50px;
        }

        @include media-breakpoint-down(md) {
          text-align: center;
        }
      }

      .cta-bar__btn {
        border-radius: 300px;
        z-index: 99;
        background-color: #d1873c;

        @include media-breakpoint-down(xl) {
          margin-top: 40px;
        }

        a {
          width: 300px;
          height: 80px;

          font-size: 1.4rem;

          @include media-breakpoint-down(sm) {
            width: 200px;
            height: 60px;

            font-size: 1.0rem;
          }
        }
      }
      .cta-bar__btn:hover {
        background-color: #dba56f;
      }
      
    }

    .cta-bar__container::after {
      content: " ";
      z-index: 4;
      background: rgb(36,51,88);
      background: linear-gradient(90deg, rgba(36,51,88,1) 18%, rgba(36,51,88,1) 33%, rgba(36,51,88,0.7514356084230567) 64%, rgba(36,51,88,0.2) 100%); 
      border-radius: 20px;
      position: absolute;
      object-fit: cover;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;

      @include media-breakpoint-down(sm) {
        border-radius: 0px;
      }
    }


  }

}
</style>