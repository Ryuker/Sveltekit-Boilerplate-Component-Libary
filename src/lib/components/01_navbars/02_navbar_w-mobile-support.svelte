<script>
  /* Navbar with mobile support

  - based on navbar on vanstooten.nl

    author: Joeri van Ees  02-08-2022
   */


   import { onMount } from 'svelte';
   import jQuery from "jquery/dist/jquery";

   onMount(async () => {


    // toggle full screen mobile menu
    jQuery('.nav-toggle').on('click', function() {
      // menu starts closed, each click toggles it
      jQuery('nav').toggleClass('menu-closed');
      jQuery('nav').toggleClass('menu-open');
      jQuery('.navbar').find('.logo').toggleClass('logo--hidden');

      // change to x icon
      jQuery(this).find('i').toggleClass('fa-times'); 
      
      // change to hamburger  icon
      jQuery(this).find('i').toggleClass('fa-bars');  
      
      // hide footer
      jQuery('footer').toggleClass('hide');          

      jQuery('body').toggleClass('mobile-nav-open');
    });

    if(jQuery(window).outerWidth() < 1400) {
      // Move icons out of links to open submenu and keep link
      var icons = jQuery('nav .menu-item-has-children a');
      jQuery(icons).each(function(index) {
        var icon = jQuery(this).children('i');
        jQuery(icon).insertAfter(jQuery(this));
      });
  
      //  jQuery('.subnav').addClass('closed');
      
      //  jQuery('nav .menu-item-has-children i').on('click', function() {
      //    jQuery(this).toggleClass('rotate');
      //    console.log(jQuery(this).parent());
      //    jQuery(this).next('.subnav').toggleClass('closed');
      //  });

      jQuery('nav .menu-item-has-children i').on('click', function() {
        jQuery(this).next('.sub-menu').toggleClass('menu-active');
        jQuery(this).parent().toggleClass('active');
        jQuery(this).toggleClass('open-icon');
      }); 
    }


    // shrink navbar on scroll

    var offset_Top = jQuery('.container__nav').offset().top;
    jQuery(document).on("scroll",function(){
      if (jQuery(document).scrollTop() > offset_Top){
        jQuery('.container__nav:not(.static)').addClass('scrolled-nav');
      }else {
        jQuery('.container__nav:not(.static)').removeClass('scrolled-nav');
      }
    });

    // return navbar to large state on mouseenter
    jQuery('.container__nav').mouseenter( function(){
      if (jQuery(document).scrollTop() > offset_Top){
        jQuery('.container__nav:not(.static)').removeClass('scrolled-nav');
      }
    });

    // return navbar to shrunk state on mouseleave
    jQuery('.container__nav').mouseleave( function(){
      if (jQuery(document).scrollTop() > offset_Top) {
        jQuery('.container__nav:not(.static)').addClass('scrolled-nav');
      }
    });
  });

</script>


<!-- Copy html starting from here -->
<div class="container__nav">
  <div class="navbar">
    <a href="/index.html" class="logo">
        <svg xmlns="http://www.w3.org/2000/svg" width="480" height="176" viewBox="0 0 480 176">
          <defs>
            <style>
              .cls-1 {
                fill-rule: evenodd;
              }
            </style>
          </defs>
          <path id="BRAND" class="cls-1" d="M40.559,46.7q11.664,0,16.776-4.1t5.112-12.312a18.15,18.15,0,0,0-1.728-8.64,12.292,12.292,0,0,0-4.752-4.9,18.717,18.717,0,0,0-6.984-2.232,66.982,66.982,0,0,0-8.424-.5H13.2V46.7h27.36ZM36.815,2.495q3.311,0,7.128.072T51.5,3a58.018,58.018,0,0,1,6.984,1.08,17.675,17.675,0,0,1,5.544,2.16A26.825,26.825,0,0,1,72.6,14.591a23.226,23.226,0,0,1,3.528,13.1,25.087,25.087,0,0,1-3.96,14.184,23.338,23.338,0,0,1-11.3,8.856v0.288q9.5,2.018,14.544,8.64a25.862,25.862,0,0,1,5.04,16.128,30.7,30.7,0,0,1-2.016,10.944,27.45,27.45,0,0,1-5.976,9.432,29.872,29.872,0,0,1-9.792,6.624,33.67,33.67,0,0,1-13.464,2.52H-0.481V2.495h37.3Zm10.656,91.3q9.072,0,14.184-4.9t5.112-13.536a16.824,16.824,0,0,0-1.872-8.352,14.544,14.544,0,0,0-4.968-5.256A20.856,20.856,0,0,0,52.8,59.015a43.365,43.365,0,0,0-8.352-.792H13.2V93.791H47.471Zm99.071-91.3q14.688,0,22.968,7.2t8.28,19.728a31.208,31.208,0,0,1-4.248,16.416q-4.249,7.057-13.608,9.648v0.288a18.336,18.336,0,0,1,7.272,2.88,15.811,15.811,0,0,1,4.464,4.824,21.911,21.911,0,0,1,2.448,6.264,66.459,66.459,0,0,1,1.224,7.2q0.286,3.746.432,7.632a65.828,65.828,0,0,0,.72,7.632,46.636,46.636,0,0,0,1.656,7.128,17.566,17.566,0,0,0,3.24,5.976H166.126a8.561,8.561,0,0,1-1.944-4.32,44.032,44.032,0,0,1-.648-6.12q-0.145-3.382-.288-7.272a50.468,50.468,0,0,0-.864-7.632q-0.577-3.743-1.44-7.128a16.752,16.752,0,0,0-2.736-5.9,13.524,13.524,0,0,0-4.9-4.032,18.163,18.163,0,0,0-8.064-1.512H111.838v43.92H98.158V2.495h48.384Zm2.88,46.656a19.768,19.768,0,0,0,7.56-2.808,15.356,15.356,0,0,0,5.184-5.616,18.858,18.858,0,0,0,1.944-9.144q0-7.776-4.32-12.672t-13.968-4.9H111.838V49.871H140.35A54.979,54.979,0,0,0,149.422,49.151Zm99.936,13.68L232.222,14.879h-0.288L214.51,62.831h34.848Zm-9.5-60.336L280.03,105.311H264.91l-11.232-30.96H210.19l-11.52,30.96H184.7L224.734,2.495h15.12Zm64.655,0,54.144,83.376h0.288V2.495H371.9V105.311H356.925L303.213,22.8h-0.288v82.512h-12.96V2.495h14.544Zm126,91.3a57.173,57.173,0,0,0,5.76-.36,32.15,32.15,0,0,0,7.344-1.728,33.553,33.553,0,0,0,7.7-3.96,26.009,26.009,0,0,0,6.84-7.056,39.437,39.437,0,0,0,4.968-11.16,58.7,58.7,0,0,0,1.944-16.2,68.889,68.889,0,0,0-1.8-16.488,31.655,31.655,0,0,0-5.9-12.384,25.961,25.961,0,0,0-10.584-7.776A42.167,42.167,0,0,0,430.8,14.015h-23.04V93.791h22.752Zm-1.152-91.3q23.76,0,36.576,12.1t12.816,36.864a83.259,83.259,0,0,1-2.88,22.968,42.937,42.937,0,0,1-8.928,16.848,38.678,38.678,0,0,1-15.408,10.44q-9.363,3.6-22.176,3.6h-35.28V2.495h35.28Z"/>
          <path id="placeholder" class="cls-1" d="M7.231,122.087v5.04H7.375a9.167,9.167,0,0,1,4.752-4.5,17.738,17.738,0,0,1,7.128-1.4,16.8,16.8,0,0,1,7.524,1.584,15.314,15.314,0,0,1,5.328,4.284,18.946,18.946,0,0,1,3.2,6.228,25.45,25.45,0,0,1,1.08,7.488,26.283,26.283,0,0,1-1.044,7.488,17.65,17.65,0,0,1-3.168,6.156,14.934,14.934,0,0,1-5.328,4.14A17.288,17.288,0,0,1,19.4,160.1a18.492,18.492,0,0,1-3.06-.288,16.983,16.983,0,0,1-3.348-.936,13.02,13.02,0,0,1-3.132-1.764,9.834,9.834,0,0,1-2.484-2.772H7.231V173.5H1.111V122.087h6.12Zm22,13.212a13.716,13.716,0,0,0-2.088-4.428,10.235,10.235,0,0,0-3.6-3.1,10.947,10.947,0,0,0-5.148-1.152,10.509,10.509,0,0,0-5.256,1.224,10.538,10.538,0,0,0-3.528,3.2,13.384,13.384,0,0,0-1.98,4.5,21.8,21.8,0,0,0,.036,10.4,13.1,13.1,0,0,0,2.052,4.5,10.478,10.478,0,0,0,3.636,3.132,11.355,11.355,0,0,0,5.4,1.188,10.456,10.456,0,0,0,5.292-1.224,9.846,9.846,0,0,0,3.42-3.24,14.1,14.1,0,0,0,1.872-4.608,24.505,24.505,0,0,0,.576-5.328A19.05,19.05,0,0,0,29.227,135.3ZM60.15,107.9v51.408H54.03V107.9h6.12Zm52.559,46.512a7.428,7.428,0,0,1-1.872.288,1.482,1.482,0,0,1-1.692-1.006,14.189,14.189,0,0,1-.252-3.161V131.424a9.99,9.99,0,0,0-1.224-5.243,8.631,8.631,0,0,0-3.24-3.125,13.1,13.1,0,0,0-4.5-1.473,34.846,34.846,0,0,0-5-.36,26.039,26.039,0,0,0-5.94.648A14.517,14.517,0,0,0,84.053,124a10.918,10.918,0,0,0-3.456,3.852,13.216,13.216,0,0,0-1.44,5.832h6.12q0.216-4.1,2.808-5.58a12.953,12.953,0,0,1,6.48-1.476,20.125,20.125,0,0,1,2.916.216,7.916,7.916,0,0,1,2.664.864,5.185,5.185,0,0,1,1.944,1.872,6.113,6.113,0,0,1,.756,3.24,3.343,3.343,0,0,1-1.008,2.628,6.651,6.651,0,0,1-2.737,1.368,26.548,26.548,0,0,1-4,.72q-2.268.253-4.788,0.756-2.376.432-4.644,1.08a13.051,13.051,0,0,0-4.032,1.908,9.424,9.424,0,0,0-2.844,3.276,10.934,10.934,0,0,0-1.08,5.184,10.78,10.78,0,0,0,.972,4.788,8.624,8.624,0,0,0,2.628,3.2,11.113,11.113,0,0,0,3.924,1.8,20.268,20.268,0,0,0,12.024-.756,14.65,14.65,0,0,0,5.868-4.356q0,3.024,1.4,4.356a5.266,5.266,0,0,0,3.78,1.332,8.669,8.669,0,0,0,4.392-.936v-4.752Zm-9.936-8.094a6.858,6.858,0,0,1-.648,2.758,8.217,8.217,0,0,1-2.016,2.723,10.936,10.936,0,0,1-3.528,2.077,14.569,14.569,0,0,1-5.184.824,12.643,12.643,0,0,1-2.736-.286,6.679,6.679,0,0,1-2.268-.931,5.078,5.078,0,0,1-1.584-1.684,4.933,4.933,0,0,1-.612-2.544,5.7,5.7,0,0,1,1.044-3.618,6.788,6.788,0,0,1,2.7-2.042,15.3,15.3,0,0,1,3.744-1.038q2.088-.322,4.14-0.574t3.924-.645a7.642,7.642,0,0,0,3.024-1.254v6.234Zm47.951-17.754a9.291,9.291,0,0,0-6.192-1.944,11.406,11.406,0,0,0-5.544,1.224,9.885,9.885,0,0,0-3.564,3.24,13.592,13.592,0,0,0-1.908,4.644,25.263,25.263,0,0,0-.576,5.436,20.647,20.647,0,0,0,.612,5.04,13.478,13.478,0,0,0,1.908,4.356,9.649,9.649,0,0,0,3.384,3.06,10.127,10.127,0,0,0,4.968,1.152A10.017,10.017,0,0,0,150.9,152.4a10.739,10.739,0,0,0,3.132-6.7H160.3q-1.01,6.912-5.148,10.656T143.884,160.1a19.4,19.4,0,0,1-7.524-1.368,14.554,14.554,0,0,1-5.472-3.888,16.777,16.777,0,0,1-3.312-6.012,25.051,25.051,0,0,1-1.116-7.668,27.32,27.32,0,0,1,1.08-7.812,18.06,18.06,0,0,1,3.276-6.336,15.37,15.37,0,0,1,5.508-4.248,18.012,18.012,0,0,1,7.7-1.548,22.508,22.508,0,0,1,5.94.756,14.5,14.5,0,0,1,4.9,2.34,12.8,12.8,0,0,1,3.492,4,14.756,14.756,0,0,1,1.728,5.724h-6.336A9.341,9.341,0,0,0,150.724,128.567Zm51.371,4.464a10.419,10.419,0,0,0-9.756-6.408,10.67,10.67,0,0,0-4.284.828,9.873,9.873,0,0,0-3.276,2.268,10.838,10.838,0,0,0-2.16,3.348,12.694,12.694,0,0,0-.936,4.068h21.384A12.572,12.572,0,0,0,202.1,133.031Zm1.476,23.9a16.894,16.894,0,0,1-10.512,3.168,19.114,19.114,0,0,1-7.74-1.44,15.241,15.241,0,0,1-5.508-4.032,17.09,17.09,0,0,1-3.348-6.192,29.749,29.749,0,0,1-1.26-7.848,22.4,22.4,0,0,1,1.3-7.776,18.577,18.577,0,0,1,3.636-6.12,16.493,16.493,0,0,1,5.544-4.032,16.92,16.92,0,0,1,7.02-1.44,15.273,15.273,0,0,1,8.244,2.052,16.323,16.323,0,0,1,5.256,5.22,20.672,20.672,0,0,1,2.736,6.912,29.686,29.686,0,0,1,.612,7.128H181.683a14.746,14.746,0,0,0,.576,4.644,10.488,10.488,0,0,0,2.088,3.888,10.284,10.284,0,0,0,3.672,2.7,12.658,12.658,0,0,0,5.256,1.008,10.593,10.593,0,0,0,6.372-1.8,8.7,8.7,0,0,0,3.276-5.472h6.048Q207.746,153.767,203.571,156.935ZM232.082,107.9v19.656h0.144a8.13,8.13,0,0,1,2.016-2.916,11.457,11.457,0,0,1,2.916-1.944,15.16,15.16,0,0,1,3.384-1.116,17.075,17.075,0,0,1,3.42-.36,16.157,16.157,0,0,1,6.12,1.008,10.089,10.089,0,0,1,3.96,2.808,10.444,10.444,0,0,1,2.124,4.284,23.086,23.086,0,0,1,.612,5.508v24.48h-6.12v-25.2a7.4,7.4,0,0,0-2.016-5.472,7.5,7.5,0,0,0-5.544-2.016,12.473,12.473,0,0,0-4.86.864,9.116,9.116,0,0,0-3.42,2.448,10.525,10.525,0,0,0-2.052,3.708,15.049,15.049,0,0,0-.684,4.644v21.024h-6.12V107.9h6.12Zm49.356,38.844a12.538,12.538,0,0,0,2.484,4.392,10.734,10.734,0,0,0,3.708,2.7,11.285,11.285,0,0,0,9,0,10.772,10.772,0,0,0,3.708-2.7,12.6,12.6,0,0,0,2.484-4.392,20.53,20.53,0,0,0,0-12.024,13.008,13.008,0,0,0-2.484-4.428,10.609,10.609,0,0,0-3.708-2.736,11.285,11.285,0,0,0-9,0,10.572,10.572,0,0,0-3.708,2.736,12.941,12.941,0,0,0-2.484,4.428A20.53,20.53,0,0,0,281.438,146.747Zm-6.228-13.68a17.352,17.352,0,0,1,3.456-6.192,16.262,16.262,0,0,1,5.688-4.14,20.844,20.844,0,0,1,15.588,0,16.372,16.372,0,0,1,5.652,4.14,17.412,17.412,0,0,1,3.456,6.192,24.822,24.822,0,0,1,1.152,7.668,24.477,24.477,0,0,1-1.152,7.632,17.452,17.452,0,0,1-3.456,6.156,15.958,15.958,0,0,1-5.652,4.1,21.316,21.316,0,0,1-15.588,0,15.857,15.857,0,0,1-5.688-4.1,17.39,17.39,0,0,1-3.456-6.156,24.418,24.418,0,0,1-1.152-7.632A24.762,24.762,0,0,1,275.21,133.067ZM333.961,107.9v51.408h-6.12V107.9h6.12Zm24.731,38.2a13.7,13.7,0,0,0,2.088,4.428,10.213,10.213,0,0,0,3.6,3.1,10.928,10.928,0,0,0,5.148,1.152,10.1,10.1,0,0,0,8.784-4.428,13.408,13.408,0,0,0,1.98-4.5,21.8,21.8,0,0,0-.036-10.4,13.105,13.105,0,0,0-2.052-4.5,10.49,10.49,0,0,0-3.636-3.132,11.36,11.36,0,0,0-5.4-1.188,10.51,10.51,0,0,0-5.256,1.224,9.764,9.764,0,0,0-3.456,3.24,14.1,14.1,0,0,0-1.872,4.608,24.426,24.426,0,0,0-.576,5.328A18.993,18.993,0,0,0,358.692,146.1Zm22,13.212v-5.04h-0.144a9,9,0,0,1-4.752,4.464,18.161,18.161,0,0,1-7.128,1.368,16.8,16.8,0,0,1-7.524-1.584,15.463,15.463,0,0,1-5.328-4.248,18.5,18.5,0,0,1-3.2-6.192,25.441,25.441,0,0,1-1.08-7.488,26.265,26.265,0,0,1,1.044-7.488,17.63,17.63,0,0,1,3.168-6.156,15.3,15.3,0,0,1,5.328-4.176,16.937,16.937,0,0,1,7.452-1.548,18.239,18.239,0,0,1,3.1.288,15.738,15.738,0,0,1,3.312.972,14.151,14.151,0,0,1,3.132,1.8,9.9,9.9,0,0,1,2.484,2.772h0.144V107.9h6.12v51.408h-6.12Zm50.507-26.28a10.49,10.49,0,0,0-2.232-3.348,10.609,10.609,0,0,0-3.312-2.232,10.486,10.486,0,0,0-4.212-.828,10.67,10.67,0,0,0-4.284.828,9.883,9.883,0,0,0-3.276,2.268,10.874,10.874,0,0,0-2.16,3.348,12.721,12.721,0,0,0-.936,4.068h21.384A12.572,12.572,0,0,0,431.2,133.031Zm1.476,23.9a16.892,16.892,0,0,1-10.512,3.168,19.117,19.117,0,0,1-7.74-1.44,15.241,15.241,0,0,1-5.508-4.032,17.12,17.12,0,0,1-3.348-6.192,29.79,29.79,0,0,1-1.26-7.848,22.4,22.4,0,0,1,1.3-7.776,18.594,18.594,0,0,1,3.636-6.12,16.5,16.5,0,0,1,5.544-4.032,16.92,16.92,0,0,1,7.02-1.44,15.273,15.273,0,0,1,8.244,2.052,16.313,16.313,0,0,1,5.256,5.22,20.651,20.651,0,0,1,2.736,6.912,29.636,29.636,0,0,1,.612,7.128H410.783a14.775,14.775,0,0,0,.576,4.644,10.488,10.488,0,0,0,2.088,3.888,10.3,10.3,0,0,0,3.672,2.7,12.658,12.658,0,0,0,5.256,1.008,10.593,10.593,0,0,0,6.372-1.8,8.7,8.7,0,0,0,3.276-5.472h6.048Q436.846,153.767,432.671,156.935Zm27.935-34.848v7.848h0.144a16.571,16.571,0,0,1,5.472-6.7,13.754,13.754,0,0,1,8.208-2.016v6.48a17.309,17.309,0,0,0-6.264,1.008,9.877,9.877,0,0,0-4.176,2.952,12.207,12.207,0,0,0-2.3,4.716,25.45,25.45,0,0,0-.72,6.372v16.56h-6.12V122.087h5.76Z"/>
        </svg>
    </a>
  
    <span class="nav-toggle">
      <a role="button"><i class="fas fa-bars"></i><span>MENU</span></a>
    </span>
  
    <nav class="menu-closed">
      <ul>
        <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children">
          <a href="filter-page.html">Aanbod <i role="button" class="fas fa-chevron-down"></i></a>
          <ul class="sub-menu">
            <li><a href="/comp-sandbox">Series III</a></li>
            <li><a href="/comp-sandbox">Defender Puma</a></li>
            <li><a href="/comp-sandbox">Defender TD5</a></li>
          </ul>
        </li>
        <li><a href="/comp-sandbox">Onderdelen</a></li>
        <li><a href="/comp-sandbox">Nieuwbouw</a></li>
        <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children">
          <a href="/comp-sandbox">Customize <i role="button" class="fas fa-chevron-down"></i></a>
          <ul class="sub-menu">
            <li><a href="/">Item #1</a></li>
            <li><a href="/">Item #2</a></li>
            <li><a href="/">Item #3</a></li>
          </ul>
        </li>
        <li><a href="/">Verkocht</a></li>
        <li><a href="/">Over ons</a></li>
        <li><a href="/">Contact</a></li>
      </ul>
    </nav>
  </div>
</div>


<div class="content-fill">
</div>

<!-- end of html content to copy -->


<style lang="scss" global>
  // @import '../../../scss/components/02_navbar';

  .content-fill {
    height: 4000px;
  }

  .container__nav {
  border-top: 4px solid white;
  position: fixed;
  width: 100%;
  height: 120px;
  z-index: 99;
  padding: 0 40px;
  transition: padding 0.2s;

  @include media-breakpoint-down (sm) {
    padding: 0 10px;
    transition: padding 0.2s;
  }

&.scrolled-nav {
  background: $white;
  height: auto;
  margin: 0;
  padding: 0 50px;
  @include media-breakpoint-down(sm) {
    padding: 0 10px;
  }
  .navbar {
    padding: 0;
    .logo {
      @include media-breakpoint-down(sm) {
        padding: 22px 10px 14px 10px;
      }
      svg {
        width: 140px;
      }
    }
    nav {
      & > ul {
        & > li {
          & > a, a:after, i {
            color: $black !important;
            @media (max-width: 1399px) {
              color: $white !important;
            }
          }
        }
      }
    }
  }
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 10px 0;
  @include media-breakpoint-down(sm) {
    padding: 10px;
  }

  .logo {
    background: white;
    margin-top: -16px;
    padding: 22px 20px 14px 20px;
    border-radius: 8px;
    z-index: 50;

    svg {
      width: 240px;
      transition: width 0.2s;

      height: auto;

      @include media-breakpoint-down(sm) {
        width: 200px;
        transition: width 0.2s;
      }
    }

    transition: width 0.5s;

    &--scrolled {
      width: 150px;
    }

    &--hidden{
      @include media-breakpoint-down(xxl) {
        opacity: 0%;
        pointer-events: none;
      }
    }
  }

  .nav-toggle {
    display: none;
    z-index: 99;
    height: 64px;
    width: 64px;
    background: $black;

    @include media-breakpoint-down(xxl) {
      display: flex;
      justify-self: end;
      justify-content: center;
      align-items: center;
      // margin-right: 30px;
      padding: 0;
    }

    a {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding-top: 5px;

      span {
        font-size: 12px;
        color: $white;
        letter-spacing: 0.1em;
        font-weight: 600;
      }
    }

    i {
      color: $white;
      font-size: 2rem;
    }
  }

  nav {
    display: flex;
    align-content: flex-start;

    & > ul {
      position: fixed;
      display: flex;
      width: 100%;
      height: 100%;
      justify-self: center;
      align-items: center;
      position: relative;

      & > li {
        position: relative;
        display: inline-flex;

        a {
          position: relative;
          display: inline-flex;
          color: $white;
          font-weight: 600;
          font-size: 1.1rem;
          padding: 0 40px;
          // @include media-breakpoint-up(xxl) {
          //   padding: 0 30px;
          // }
          @media (max-width: 1580px) {
            font-size: 1rem;
            padding:0 30px;
          }
        }

        &.menu-item-has-children {
          & > a {
            i {
              color: #fff;
              position: absolute;
              top: 4px;
              right: 18px;
              font-weight: 700;
              @media (max-width: 1580px) {
                right: 10px;
              }
            }
          }
        }

        // span {
        //   width: 100%;
        //   display: inline-flex;
        //   color: white;
        //   align-items: center;
        //   justify-content: space-between;

        //   i {
        //     // height: 50px;
        //     // width: 50px;
        //     font-size: 1.2rem;
        //     display: flex;
        //     align-items: center;
        //     justify-content: center;

        //     &.open-icon {
        //       transform: rotate(-180deg);
        //       transform-origin: center;
        //     }
        //   }
        // }

        // &:hover {
        //   & > a:hover {
        //     // color: $blue;
        //   }

        //   & > span > i:hover {
        //     color: $blue;
        //   }
        // }

        & > ul {
          position: absolute;
          display: flex;
          flex-direction: column;
          width: fit-content;
          height: fit-content;
          top: 100%;
          align-self: flex-start;
          align-items: flex-start;
          min-width: 100%;
          width: max-content;
          left: 0;
          padding-top:24px;
          
          & > li {
            display: inline-flex;
            justify-content: flex-start;
            flex-wrap: nowrap;
            width: 100%;
            
            & > a {
              color: $white;
              background: $black;
              width: 100%;
              padding: 10px 24px;

              &:hover{
                background: $blue;
                color: $white;
              }
            }

            &:hover {
              @include media-breakpoint-up(xxl){
                background-color: $blue;
              }
            }
          }
        }

        &.active {
          @include media-breakpoint-up(xxl) {
            background: $black;
          }
        }

        & > .sub-menu {
          display: none;
        }

        @include media-breakpoint-up(xxl) {
          &:hover {
            .sub-menu{
              display: flex;
              // background: $black;
            }
          }
        }

        .sub-menu.menu-active {
          display: flex;
          background: $black;
        }
      }

      &.mobile-visible {
        display: flex;
      }
    }

    &.menu-closed {
      @include media-breakpoint-down(xxl) {
        display: none;
      }
    }

   &.menu-open {
      @include media-breakpoint-down(xxl) {
        position: fixed;
        width: 100%;
        height: 100%;
        background: $black;
        top: 0;
        left: 0;
        padding: 6rem 40px 200px;
        z-index: 80;
        overflow: scroll;

        & > ul {
          flex-direction: column;
          align-items: flex-start;
          display: flex;
          width: 100%;
          height: fit-content;
          z-index: 99;
          color: white;

          li {
            width: 100%;
            position: relative;
            display: flex!important;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            flex-direction: row;
            i {
              height: 40px;
              width: 40px;
              display: flex;
              justify-content: center;
              align-items: center;
              &.open-icon {
                transform: rotate(-180deg);
                transform-origin: center;
              }
            }
            a { 
              padding: 20px 30px;
              flex: 1 0 auto;
              color: white;
              font-size: 1.6rem;
              @include media-breakpoint-down(md) {
                font-size: 1.4rem;
                padding: 20px 0;
              }
              &:hover {
                color: $blue;
              }
            }

            & > ul {
              display: none;

              &.menu-active {
                position: relative;
                color: white;
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                padding-top: 0;
                padding-bottom: 30px;

                li {
                  padding: 0;
                  display: block;

                  a {
                    padding: 5 30px;
                    font-size: 1.3rem;
                    &:hover {
                      background: none;

                    }
                  }
                }                
              }
            }
            
            &.active {
              
              & > span {
                border-bottom: 1px solid white;
              }
            }
          }
        }
      }
    }
  }
}
}


.mobile-nav-open {
overflow: hidden;
height: 100vh;
}
</style>
