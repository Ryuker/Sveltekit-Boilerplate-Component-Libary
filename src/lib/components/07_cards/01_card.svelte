<script>
  /* single card
    - basic rounded card with center text
    - supports img as bg
    - supports color of bg (add .bg-[insertcolor name] )

    author: Joeri van Ees 
  */ 
</script>

<h2>single card variations</h2>
<div style="display: flex; flex-direction: row">
  <div class="card">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>

    <div class="card-inner">
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
    </div>
    
  </div>
  
  <div class="card bg-red">
    <div class="card-inner">
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
    </div>
    
  </div>
  
  <div class="card bg-blue">
    <div class="card-inner">
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
    </div>
    
  </div>

  <div class="card">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>
    <div class="card-inner">
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
    </div>
  </div>
</div>


<style lang="scss">

.card {
  margin: 10px;
  position: relative;
  width: 300px;
  height: 200px;
  border-radius: 25px;
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    position: absolute;
    border-radius: 25px;
    width: 100%;
    height: 100%;

    opacity: 0.5;
    z-index: 1;
  }

  .card-inner {
    display: flex;
    width: 100%;
    height: 100%;
    padding: 15px 0px;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    align-items: center;
    // text-align: center;
    z-index: 10;

    h3 {
      margin: 0;
      z-index: 10;
    }

    span {
      padding: 10px;
      position: relative;
      font-size: 0.8rem;
      z-index: 10;
      color: black;
    }
  }
}

.card {
  &.bg-red {
    background: rgb(236, 90, 90);
  }

  &.bg-blue {
    background: rgb(123, 123, 208);

    span {
      color: white;
    }
  }
}

</style>