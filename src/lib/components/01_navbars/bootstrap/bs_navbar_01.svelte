<script>
  /* Function of Component:
  desktop > ipad
    brand + Left aligned menu
  mobile:
    brand + hamburger menu

  author: Joeri van Ees - 28-03-2022
  */
  import { onMount } from 'svelte';
  import jQuery from 'jquery/dist/jquery';
  
  onMount(async() => {
    jQuery('.nav-toggle').on('click', function() {
      console.log("clicked"); // REMOVE AFTER TESTING

      if (!jQuery('.menu-open')[0]) { // menu is closed, so open the menu
        console.log("opening menu");
        
        jQuery(this).toggleClass('nav-toggle-open');
        jQuery('.menu').addClass('menu-open');
        jQuery('body').addClass('mobile-nav-open');
      } else {                        // menu is open, so close the menu
        console.log("closing menu");
        jQuery('.menu').removeClass('menu-open');
        jQuery('body').removeClass('mobile-nav-open');
      }
    });
  });

  // for reference. Delete after menu is functional
  //   if (!jQuery('.menu-open')[0]) {
  //     jQuery(this).toggleClass('nav-toggle-open');
  //     jQuery('.menu').addClass('menu-open');
  //     jQuery(this).find('i').removeClass('fa-bars');
  //     jQuery(this).find('i').addClass('fa-times');
  //     jQuery('body').addClass('mobile-nav-open');
  //   } else {
  //     jQuery('.nav-toggle i').removeClass('fa-times');
  //     jQuery('.nav-toggle i').addClass('fa-bars');
  //     jQuery('.menu').removeClass('menu-open');
  //     jQuery('body').removeClass('mobile-nav-open');
  //   }
  // });

  // onMount(() => {
  //   const jq = window.$; 
  // });


</script>

<!-- copyable component code goes here -->
<div class="navbar">
  <div class="container">
    <a href="/comp-sandbox" class="logo"><img src="static/placeholders/brand_placeholder.svg" alt="brand"></a>
    <nav class="nav__menu">
      <!-- displays hamburger menu when below LG screen width -->
      
      <!-- display in-line menu when above LG screen width -->
      <ul>
        <li><a href="/comp-sandbox">Link #1</a></li>
        <li><a href="/comp-sandbox">Link #2</a></li>
        <li><a href="/comp-sandbox">Link #3</a></li>
        <li><a href="/comp-sandbox">Link #4</a></li>
        <li><a href="/comp-sandbox">Link #5</a></li>
      </ul>
    </nav>

    <span class="mobile-toggle">
      <a href="/comp-sandbox">
        <i class="menu-icon nav-toggle"><svg  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 96C0 78.33 14.33 64 32 64H416C433.7 64 448 78.33 448 96C448 113.7 433.7 128 416 128H32C14.33 128 0 113.7 0 96zM0 256C0 238.3 14.33 224 32 224H416C433.7 224 448 238.3 448 256C448 273.7 433.7 288 416 288H32C14.33 288 0 273.7 0 256zM416 448H32C14.33 448 0 433.7 0 416C0 398.3 14.33 384 32 384H416C433.7 384 448 398.3 448 416C448 433.7 433.7 448 416 448z"/></svg></i>
      </a>
    </span>
  </div>
</div>





<style lang="scss">

  h4 {
    text-align: left;
  }

 .menu-icon {
    svg {
      width: 40px;
    }
  }

  .navbar {
    background-color: rgb(192, 193, 238);
    position: relative;
    // width: 100%;
    display: block;
    padding: 0px 20px;

    // background-color: aqua;
    
    height: 100px;

    .logo {
      img {
      width: 200px;
      }
    }

    .container {
      // background-color: purple;

      display: flex;
      justify-content: space-between;
      padding: 0;
      align-items: center;
      height:100%;

      .nav__menu {
        text-align: right;
        height: 100%;
        

        ul {
          // background-color: green;
          text-align: right;
          display: flex;
          align-items: center;
          
          list-style: none;
          height: 100%;
          margin: 0;

          li {
            // background-color: aqua;
            
            padding: 0 20px;
            height: 100%;
            
            a {
              display: flex;
              // background-color: red;
              align-items: center;
              
              text-decoration: none;
              height: 100%;
            }

            a:hover {
              color: blue;
            }
          }
        }


        .menu-open {
          background-color: red;
          position: fixed;
          height: 400px;
        }

        @include media-breakpoint-down(lg) {
          background-color: green;
          position: fixed;
          display: flex;
          display:none;
          flex-direction: column;
          justify-content:flex-end;
         
          top: 0px;
          left: 0px;
          // left: 60px;
          width: 50%;
          height: 100%;
          // background-color: red;
          align-items: center;
          opacity: 0.8;

          ul {
              
              // background-color: green;
              display: flex;
              flex-direction: column;
              align-items: right;
              padding: 0;
            }

        }
      }
      .mobile-toggle {
        display: none;
        justify-content: end;
        text-align: right;
        align-items: center;

        @include media-breakpoint-down(lg) {
          display: flex;
          align-items: center;
          height: 100%;

          a:hover {
            color: blue;
          }

          .nav__menu {
            

           
          }
        }
      }

      .mobile-nav-open {
        background-color: red;
        height: 400px;
        
      }
    // change position to fixed when scrollin
    }
  }
</style>

<!-- copyable component code ends here -->