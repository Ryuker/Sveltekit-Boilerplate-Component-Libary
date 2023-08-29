<script>
  /* card - varying sizes
    - basic rounded card with center text
    - supports img as bg
    - supports color of bg (add .bg-[insertcolor name] )

    author: Joeri van Ees 
  */ 
</script>


<h2>single card varying sizes</h2>
<div style="display: flex; flex-direction: row">
  <div class="card card--large">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>

    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. 
      In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum.  </span>
      <a href="/comp-builder">Learn More</a>
    </div>
    
  </div>
  
  <div class="card bg-red">
    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
      <a href="/comp-builder">Learn More</a>
    </div>
  </div>
  
  <div class="card bg-blue">
    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
      <a href="/comp-builder">Learn More</a>
    </div>
  </div>

  <div class="card bg-blue">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>
    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
      <a href="/comp-builder">Learn More</a>
    </div>
  </div>
</div>


<div style="display: flex; flex-direction: row">
  
  <div class="card bg-red">
    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
      <a href="/comp-builder">Learn More</a>
    </div>
  </div>

  <div class="card bg-blue">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>
    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
        sed mi tincidunt fermentum. </span>
      <a href="/comp-builder">Learn More</a>
    </div>
  </div>

  <div class="card card--large">
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>

    <div class="card-inner">
      <h3>Some Heading</h3>
      <span>In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. 
      In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum. In aliquam ipsum sed mi tincidunt fermentum.
      sed mi tincidunt fermentum.  </span>
      <a href="/comp-builder">Learn More</a>
    </div>
    
  </div>
</div>


<style lang="scss">

.card {
  margin: 10px;
  position: relative;
  width: 300px;
  min-height: 200px;
  height: auto;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  .card-inner {
    display: flex;
    width: 100%;
    height: 100%;
    padding: 15px 0px;
    flex-direction: column;
    justify-content: flex-end;
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

      // text-align: center;
    }

    a {
      margin-top: 20px;
      padding: 10px 10px;
      background: rgb(46, 51, 103);
      width: 100px;
      color: white;
      border-radius: 25px;
      text-decoration: none;
      z-index: 10;
      text-align: center;
    }
  }

  img {
    position: absolute;
    border-radius: 25px;
    width: 100%;
    height: 100%;

    opacity: 0.5;
    z-index: 1;
    object-fit: cover;
  }
}

.card {
  &.bg-red {
    background: rgb(236, 90, 90);
  }

  &.bg-blue {
    background: rgb(123, 123, 208);

    span, h3 {
      color: white;
    }
  }
}

.card--large {
  width: 80%;
}

</style>