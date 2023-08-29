<script>
  /* icons row - responsive w 100% per icon at 
    - basic icons row
    - scales down at mid size rez
    - responsively icons 
        - take up 50% of div below MD width
        - take up 100% of div below SM width

    author: Joeri van Ees 
  */ 

</script>

<h3>icons row - w50 % below MD | w 100% below SM</h3>
<div class="icons-row">
  <div class="icon">
    <i class="fa-solid fa-feather-pointed"></i>
    <span>service 1</span>
  </div>
  <div class="icon">
    <i class="fa-solid fa-atom"></i>
    <span>service 2</span>
  </div>
  <div class="icon">
    <i class="fa-solid fa-anchor"></i>
    <span>service 3</span>
  </div>
  <!-- TODO - add font awesome to i, a -->

  <div class="icon">
    <i class="fa-solid fa-brush"></i>
    <span>service 3</span>
  </div>
  
  
</div>


<style lang="scss">
.icons-row {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-content: center;
  margin-bottom: 60px;

  @include media-breakpoint-down(md) {
    flex-wrap: wrap;

    .icon {
      width: 50%;
      align-items: center;
      margin-bottom: 60px;

      i {
        font-size: 4.0rem;
      }
    }

    // remove margin bottom from last 2 childs
    .icon:nth-last-child(-n+2){
      margin-bottom: 0;
    }
  }

  @include media-breakpoint-down(sm) {

    .icon {
      width: 100%;
      align-items: center;

      i {
        font-size: 4.0rem;
      }
    }

      
    .icon:nth-last-child(n){
      margin-bottom: 60px;
    }

    // remove margin bottom from last child

    .icon:nth-last-child(-n+1){
      margin-bottom: 0;
    }
  }
  


  .icon {
    background-color: aqua;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    padding: 10px 0px;


    i {
      font-size: 6.0rem;
    }

    span {
      margin-top: 10px;
      background: red;
      text-align: center;
    }
  }
}


</style>