<script>
  /* card - without bg image
    - basic card with img + heading + text + button
    - supports color add .bg-[insertcolor name] )

    author: Joeri van Ees 
  */ 
</script>


<h2>card without bg-image</h2>
<div style="display: flex; flex-direction: row">
  <div class="card card--large bg-blue">
    <!-- <img class="bg" src="./static/placeholders/stock-image.jpeg" alt="card-bg"/> -->
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
    <img src="./static/placeholders/stock-image.jpeg" alt="card-bg"/>
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

</div>


<style lang="scss">

.card {
  margin: 10px;
  position: relative;
  width: 300px;
  min-height: 200px;
  height: fit-content;
  // border-radius: 25px;
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
    // position: absolute;
    // border-radius: 25px;
    width: 100%;
    height:40%;

    opacity: 0.9;
    z-index: 10;
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
  width: 50%;
  height: 80%;
}

</style>