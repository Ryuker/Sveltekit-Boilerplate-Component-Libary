<script>
	/* Div Filter 
    - Filters a list of a elements with figures, text and a table each
    - Filter using buttons
    - using data-filter to filter divs.

    - used on vanstooten.nl

    author: Joeri van Ees - created: 10/08/2022
  */

	import { onMount } from 'svelte';
	import jQuery from 'jquery/dist/jquery';

	onMount(async () => {
		const module = await import('slick-carousel');    // import jquery

		jQuery(document).ready(function () {
			roverFilter();
		});

		jQuery(window).resize(function () {
			roverFilter();
		});

		function roverFilter() {
			if (jQuery(window).width() > 992) {
				var filterElement = jQuery('.rov-filter');
				jQuery(filterElement).replaceTagName('div');

				jQuery('body').on('click', '.rov-filter-option', function () {
					jQuery('.rov-filter-option').removeClass('active');
					jQuery(this).addClass('active');
					var filter = jQuery(this).data('filter').toString();
					// console.log(filter);
					jQuery('.rov-item').each(function () {
						var tax = jQuery(this).data('filter').toString().split(',');
						// console.log(tax);
						if (tax.indexOf(filter) > -1) {
							jQuery(this).show();
						} else {
							jQuery(this).hide();
						}
					});
				});
			} else {
				var filterElement = jQuery('.rov-filter');
				var filterOptions = jQuery(filterElement).children();
				jQuery(filterOptions).each(function () {
					jQuery(this).replaceTagName('option');
				});

				jQuery(filterElement).replaceTagName('select');

				jQuery('body').on('change', '.rov-filter', function () {
					var optionSelected = jQuery('option:selected', this);
					optionSelected = jQuery(optionSelected).data('filter').toString();
					var valueSelected = this.value;

					jQuery('.rov-item').each(function () {
						var tax = jQuery(this).data('filter').toString().split(',');
						if (tax.indexOf(optionSelected) > -1) {
							jQuery(this).show();
						} else {
							jQuery(this).hide();
						}
					});
				});
			}
		}

		// filter code
		(function (a) {
			a.fn.replaceTagName = function (f) {
				var g = [],
					h = this.length;
				while (h--) {
					var k = document.createElement(f),
						b = this[h],
						d = b.attributes;
					for (var c = d.length - 1; c >= 0; c--) {
						var j = d[c];
						k.setAttribute(j.name, j.value);
					}
					k.innerHTML = b.innerHTML;
					a(b).after(k).remove();
					g[h - 1] = k;
				}
				return a(g);
			};
		})(module.jQuery);


		// copy below code to boilerplate for filter
		// function (a) {
		// 	a.fn.replaceTagName = function (f) {
		// 		var g = [],
		// 			h = this.length;
		// 		while (h--) {
		// 			var k = document.createElement(f),
		// 				b = this[h],
		// 				d = b.attributes;
		// 			for (var c = d.length - 1; c >= 0; c--) {
		// 				var j = d[c];
		// 				k.setAttribute(j.name, j.value);
		// 			}
		// 			k.innerHTML = b.innerHTML;
		// 			a(b).after(k).remove();
		// 			g[h - 1] = k;
		// 		}
		// 		return a(g);
		// 	};
		//})(window.jQuery);
	});
</script>

<section class="container">
	<div class="container__header">
		<h1>Aanbod</h1>
	</div>
	<div class="row">
		<div class="col-12">
			<div class="rov-filter">
				<a class="button active rov-filter-option me-2" data-filter="all">Alle</a>
				<a class="button rov-filter-option me-2" data-filter="1">Series III</a>
				<a class="button rov-filter-option me-2" data-filter="2">Defender Puma</a>
				<a class="button rov-filter-option me-2" data-filter="3">Defender TD5</a>
			</div>
		</div>
		<div class="col-12">
			<div class="row gx-5 rov-filter-results">
				<a href="/comp-builder" class="col-12 col-sm-6 rov-item mb-4" data-filter="all,1">
					<figure>
						<img src="https://source.unsplash.com/random/300×300/?engine&1/" alt="" />
					</figure>
					<div class="rov-item-content">
						<div class="offer__header__title">
							<span class="year">2003</span>
							<h2>Land Rover<br />Defender Puma</h2>
						</div>
						<table>
							<tbody>
								<tr>
									<td class="info-label">Prijs:</td>
									<td>€41.000,-</td>
								</tr>
								<tr>
									<td class="info-label">KM-stand:</td>
									<td>21.000</td>
								</tr>
							</tbody>
						</table>
					</div>
				</a>

				<a href="/comp-builder" class="col-12 col-sm-6 rov-item mb-4" data-filter="all,2">
					<figure>
						<img src="https://source.unsplash.com/random/300×300/?engine&2/" alt="" />
					</figure>
					<div class="rov-item-content">
						<div class="offer__header__title">
							<span class="year">2003</span>
							<h2>Land Rover<br />Defender Puma</h2>
						</div>
						<table>
							<tbody>
								<tr>
									<td class="info-label">Prijs:</td>
									<td>€41.000,-</td>
								</tr>
								<tr>
									<td class="info-label">KM-stand:</td>
									<td>21.000</td>
								</tr>
							</tbody>
						</table>
					</div>
				</a>

				<a href="/comp-builder" class="col-12 col-sm-6 rov-item mb-4" data-filter="all,3">
					<figure>
						<img src="https://source.unsplash.com/random/300×300/?engine&3/" alt="" />
					</figure>
					<div class="rov-item-content">
						<div class="offer__header__title">
							<span class="year">2003</span>
							<h2>Land Rover<br />Defender Puma</h2>
						</div>
						<table>
							<tbody>
								<tr>
									<td class="info-label">Prijs:</td>
									<td>€41.000,-</td>
								</tr>
								<tr>
									<td class="info-label">KM-stand:</td>
									<td>21.000</td>
								</tr>
							</tbody>
						</table>
					</div>
				</a>

				<a href="/comp-builder" class="col-12 col-sm-6 rov-item mb-4" data-filter="all,1">
					<figure>
						<img src="https://source.unsplash.com/random/300×300/?engine&4/" alt="" />
					</figure>
					<div class="rov-item-content">
						<div class="offer__header__title">
							<span class="year">2003</span>
							<h2>Land Rover<br />Defender Puma</h2>
						</div>
						<table>
							<tbody>
								<tr>
									<td class="info-label">Prijs:</td>
									<td>€41.000,-</td>
								</tr>
								<tr>
									<td class="info-label">KM-stand:</td>
									<td>21.000</td>
								</tr>
							</tbody>
						</table>
					</div>
				</a>
			</div>
		</div>
	</div>
</section>

<style lang="scss" global>
	.container {
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 1400px;
		padding: 140px 40px 0;
		margin: 0 auto;
		@include media-breakpoint-down(md) {
			padding: 100px 20px 0;
		}
	}

	.container {
		&__header {
			display: block;
			margin: 30px 0;
			h1 {
				font-weight: 800;
				text-transform: uppercase;
				color: $black;
				margin-bottom: 0;
			}
		}

		figure {
			position: relative;
			height: 0;
			width: 100%;
			padding-bottom: 64.75%;
			margin-bottom: 30px;
			img {
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				object-fit: cover;
				object-position: center;
			}
		}
	}

	.rov-filter {
		margin: 0 0 40px 0;
		.button {
			background: $black;
			&.active,
			&:hover {
				color: white;
				background: $blue;
				transition: 0.2s ease;
			}
		}
	}

	.rov-item {
		figure {
			overflow: hidden;
			background: $black;
			margin-bottom: 10px;
			img {
				transition: 1.5s ease-out;
			}
		}
		&:hover {
			img {
				opacity: 0.75;
				transform: scale(1.1);
				transition: 2.3s ease;
			}
		}
		.rov-item-content {
			display: flex;
			align-items: flex-end;
			padding-bottom: 30px;
			@include media-breakpoint-down(lg) {
				flex-direction: column;
				align-items: flex-start;
			}
			h2 {
				text-transform: uppercase;
				font-weight: 900;
				font-size: 2.1rem;
				margin: 0;
				color: $black;
				@include media-breakpoint-down(xl) {
					font-size: 1.8rem;
				}
			}
			.year {
				font-size: 1.35rem;
				padding: 0 7px;
				@include media-breakpoint-down(xl) {
					font-size: 1.2rem;
				}
			}
			table {
				width: 40%;
				font-size: 1.1rem;
				color: $black;
				text-align: right;
				td {
					padding-top: 10px 0 5px;
				}
				@include media-breakpoint-down(xl) {
					font-size: 1rem;
				}
				@include media-breakpoint-down(lg) {
					margin-top: 15px;
					text-align: left;
					width: 100%;
				}
				.info-label {
					font-weight: bold;
					padding-right: 15px;
				}
			}
		}
		@include media-breakpoint-down(lg) {
			display: flex;
			flex-direction: column;
		}
	}

	select.rov-filter {
		position: relative;
		background-color: $black !important;
		font-size: 1rem;
		color: $white;
		display: flex;
		min-width: 250px;
		max-width: 100%;
		align-items: center;
		padding: 10px 14px;
		justify-content: center;
		font-weight: bold;
		box-shadow: none !important;
		border-radius: 0;
		background-image: url(https://rm1.tempurl.host/wp-content/themes/gamebasics/images/arrow-down.svg) !important;
		background-repeat: no-repeat !important;
		background-position: center right 15px !important;
		-webkit-appearance: none;
		appearance: none;
	}
</style>
