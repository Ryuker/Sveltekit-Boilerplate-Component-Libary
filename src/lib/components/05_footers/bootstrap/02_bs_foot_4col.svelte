<script>
	/* Bootstrap Footer 02 - 4 columns responsive
  - 4 columns
  - - desktop: 4 col , tablet: 2 col, mobile: 1 col
  - inline menu for open positions, FAQ and other
  - copyright bar

  author: Joeri van Ees 
  used on: heightspecialists.com
  */
</script>

<!-- copyable component code goes here -->
<footer>
	<section class="container">
		<!-- open posiitions, FAQ, other -->
	
		<!-- 4 columns -->
		<div class="row gx-0 mt-5 pt-5">
			<div class="col-xs-12 col-md-6 col-lg-3 mb-5">
				<h4>Heading #1</h4>
				<ul class="nolist">
					<li><a href="/comp-sandbox">Link #1</a></li>
					<li><a href="/comp-sandbox">Link #2</a></li>
					<li><a href="/comp-sandbox">Link #3</a></li>
					<li><a href="/comp-sandbox">Link #4</a></li>
					<li><a href="/comp-sandbox">Link #5</a></li>
				</ul>
			</div>
			<div class="col-xs-12 col-md-6 col-lg-3 mb-5">
				<h4>Heading #2</h4>
				<ul class="nolist">
					<li><a href="/comp-sandbox">Link #1</a></li>
					<li><a href="/comp-sandbox">Link #2</a></li>
					<li><a href="/comp-sandbox">Link #3</a></li>
					<li><a href="/comp-sandbox">Link #4</a></li>
					<li><a href="/comp-sandbox">Link #5</a></li>
				</ul>
			</div>
			<div class="col-xs-12 col-md-6 col-lg-3 mb-5">
				<h4>Heading #3</h4>
				<ul class="nolist">
					<li><a href="/comp-sandbox">Link #1</a></li>
					<li><a href="/comp-sandbox">Link #2</a></li>
					<li><a href="/comp-sandbox">Link #3</a></li>
					<li><a href="/comp-sandbox">Link #4</a></li>
					<li><a href="/comp-sandbox">Link #5</a></li>
				</ul>
			</div>
			<div class="col-xs-12 col-md-6 col-lg-3 mb-5">
				<h4>Heading #4</h4>
				<ul class="nolist">
					<li><a href="/comp-sandbox">Link #1</a></li>
					<li><a href="/comp-sandbox">Link #2</a></li>
					<li><a href="/comp-sandbox">Link #3</a></li>
					<li><a href="/comp-sandbox">Link #4</a></li>
					<li><a href="/comp-sandbox">Link #5</a></li>
				</ul>
			</div>
		</div>
	</section>
	<section id="copyright" class="container">
		<div class="row justify-content-between margins align-items-center">
			<div class="col-lg-auto d-sm-flex align-items-center">
				<span>Company Name</span>
				<span class="divider" />
				<a href="/comp-sandbox" >
				  <div class="social-media d-sm-inline-block">
						<a class="social-icon" href="/comp-sandbox">
							<i class="fa-brands fa-facebook"></i>
						</a>

						<a class="social-icon" href="/comp-sandbox">
							<i class="fa-brands fa-facebook"></i>
						</a>

						<a class="social-icon" href="/comp-sandbox">
							<i class="fa-brands fa-facebook"></i>
						</a>
				</div>
			</div>
			<div class="col-lg-auto ml-lg-5 emblems d-md-inline-block">
				<a target="_blank" class="d-inline-block" href="<?php the_sub_field('link');?>">
					<img class="mr-2" height="48" src="<?php the_sub_field('quality_mark');?>" alt="" />
				</a>
			</div>
		</div>
    <div class="row justify-content-between">
			<div id="footer-logo" class="col-md-auto">
				<a href="/comp-sandbox">
					<img src="static/placeholders/brand_placeholder.svg" height="60" alt="" />
				</a>
			</div>
			<nav class="col-md-auto">
				<ul class="nolist">
					<li><a href="/comp-sandbox">Open Positions</a></li>
					<li><a href="/comp-sandbox">Frequently Asked Questions</a></li>
          <li><a href="/comp-sandbox">Other</a></li>
				</ul>
			</nav>
		</div>
	</section>
</footer>

<style lang="scss">
	/* footer 4 columns */
	footer {
    .container {
      h4 {
			margin-bottom: 1em;
			color: rgb(85, 19, 19);
      text-align: left;
		}
		ul {
			padding: 0;
			margin: 0;
			list-style: none;

      .nolist {
        list-style: none;
		    background-color: red;
      }
			li {
				text-align: left;
				text-decoration: none;
				a {
					display: block;
					padding: 6px 0px;
					text-decoration: none;
					font-size: 16px;
				}
			}
		}
		#copyright {
			margin-top: 40px !important;
		}

    }
		
	}
</style>
