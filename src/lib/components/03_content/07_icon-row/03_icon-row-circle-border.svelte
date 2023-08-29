<script>
  /* icons row - stacked on circle
    - basic icons row
    - scales down at mid size rez
    - responsively icons 
        - take up 50% of div below MD width
        - take up 100% of div below SM width

    author: Joeri van Ees 
  */ 

</script>

<h3>icons row - stacked on circle</h3>
<div class="icons-row">
  <div class="icon">
    <span class="fa-stack large">
      <i class="fa-regular fa-circle fa-stack-2x"></i>
      <i class="fa-solid fa-feather-pointed fa-stack-1x"></i>
    </span>
    <span>service 1</span>
  </div>

  <div class="icon">
    <span class="fa-stack large">
      <i class="fa-regular fa-circle fa-stack-2x"></i>
      <i class="fa-solid fa-atom fa-stack-1x"></i>
    </span>
    <span>service 2</span>
  </div>

  <div class="icon">
    <span class="fa-stack large">
      <i class="fa-regular fa-circle fa-stack-2x"></i>
      <i class="fa-solid fa-anchor fa-stack-1x"></i>
    </span>
    <span>service 3</span>
  </div>

  <div class="icon">
    <span class="fa-stack large">
      <i class="fa-regular fa-circle fa-stack-2x"></i>
      <i class="fa-solid fa-brush fa-stack-1x"></i>
    </span>
    <span>service 4</span>
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

      .fa-stack.large { 
        font-size: 3.0rem; 
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

      .fa-stack.large { 
        font-size: 2.0rem; 
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
    // padding: 10px 0;

    span.fa-stack.large {
      // margin-top: 10px;
      background: red;
      text-align: center;
      display: flex;
      align-self: center;
      padding: 10px 0px;
      font-size: 3.0rem;  
    }

    i {
      vertical-align: middle; 
    }

    span {
      text-align: center;
    }
  }
}


</style>