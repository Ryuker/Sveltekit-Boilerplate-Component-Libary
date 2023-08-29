<ul>
  <li><a href="/">Index</a></li>
  <li><a href="/about">About</a></li>
  <li><a href="/bootstrap_test">Bootstrap_Test</a></li>
  <li><a href="/comp-sandbox">Component_SB</a></li>
  <li><a href="/comp-builder">Component_Builder</a></li>
  
</ul>

<style lang="scss"> 

  ul {
    text-align: center;
    display: flex;
    flex-direction: row;
    list-style-type: none;
    justify-content: center;
    padding: 0;
    margin: 0;

    text-decoration: none;

    li{
      padding: 10px;
      text-decoration: none;

      a {
        text-decoration: none;
      }

      @include media-breakpoint-down(sm)
      {
        padding: 5px;
      }
    }  
  }
</style>