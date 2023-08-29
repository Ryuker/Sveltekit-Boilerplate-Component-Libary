<script>
  /* Video list
    - video's listed under each other on all rez
    - max width
  */ 

</script>


<div class="video-list">
  <video  controls poster="./media/01_introduction_small.png">
    <source src="http://clips.vorwaerts-gmbh.de/VfE_html5.mp4" type="video/mp4">
  </video>

  <video  controls poster="./media/01_introduction_small.png">
    <source src="http://clips.vorwaerts-gmbh.de/VfE_html5.mp4" type="video/mp4">
  </video>

  <video  controls poster="./media/01_introduction_small.png">
    <source src="http://clips.vorwaerts-gmbh.de/VfE_html5.mp4" type="video/mp4">
  </video>
</div>



<style lang="scss">

.video-list {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;

  video {
    display: block;
    width: 100%;
    max-width: 800px;
    margin-bottom: 80px;
  }
}
</style>