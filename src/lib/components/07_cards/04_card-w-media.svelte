<script>
  /* card with media
    - basic rounded card with center text
    - supports img as bg
    - supports color of bg (add .bg-[insertcolor name] )

    author: Joeri van Ees 
  */ 
</script>

<h2>single card with video</h2>
<div style="display: flex; flex-direction: row">
  <div class="card">
    <div class="video-container">
      <video  controls poster="./static/placeholders/stock-image.jpeg">
        <source src="http://clips.vorwaerts-gmbh.de/VfE_html5.mp4" type="video/mp4">
      </video>
    </div>
  </div>

  <div class="card">
    <div class="video-container">
      <video  controls poster="./static/placeholders/stock-image.jpeg">
        <source src="http://clips.vorwaerts-gmbh.de/VfE_html5.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>


<style lang="scss">

.card {
  margin: 40px 10px;
  position: relative;
  width: 300px;
  height: 250px;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  .video-container {
    padding: 0;
    margin: 0;
    border-radius: 25px;
    width: 100%;
    height: 0;
    padding-bottom: 67.743%;
    position: relative;
  }

  video {
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 25px;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  span {
    padding: 10px;
    position: relative;
    font-size: 0.8rem;
    z-index: 10;
    color: black;

    text-align: center;
  }

  h3 {
    margin: 0;
    z-index: 10;
  }

  a {
    margin-top: 20px;
    padding: 10px 20px;
    background: rgb(46, 51, 103);
    color: white;
    border-radius: 25px;
    text-decoration: none;
    z-index: 10;
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

</style>