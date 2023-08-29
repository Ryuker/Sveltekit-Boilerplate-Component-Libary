<script>
  /* Copyright Bar Minimal 
  - centered copyright text on all resolutions

  author: Joeri van Ees - 06-04-2022
  */
</script>


<div class="copyright-bar">
  <div class="cb__wrapper">
    <span class="copyright">© 2022. Brand B.V. All Rights Reserved</span>
  </div>
</div>


<style lang="scss">

.copyright-bar {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  height: 100px;
  background-color: rgb(224, 112, 0);
  width: 100%;
  
  .cb__wrapper {
    display: flex;
    align-items: center;
    width: 100%;
    justify-content: center;
    height: 100%;

    .copyright {
      background-color: rgb(46, 141, 199);
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-wrap: wrap;
      color: $white;
    }
  }
}

</style>