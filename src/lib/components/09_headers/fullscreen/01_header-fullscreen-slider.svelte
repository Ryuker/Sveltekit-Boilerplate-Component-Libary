<svelte:head>
	<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
</svelte:head>

<script>
	/* Header Fullscreen Slider

  - covers full browser width and height(without scrolling)
  - uses slick slider

  - based on fullscreen header on vanstooten.nl

    author: Joeri van Ees  02-08-2022
   */


	 import { onMount } from 'svelte';
   import jQuery from "jquery/dist/jquery";

   onMount(async () => {
    const module = await import('slick-carousel');    // import jquery

    jQuery('.slider').on('click', function() { // test if jquery is working
      console.log("click");
    })

    // fullscreen image slider
    // navigation
    jQuery('.slider-nav-prev').click(function(){
      jQuery('.full-screen-media-slider').slick('slickPrev');
    })

    jQuery('.slider-nav-next').click(function(){
      jQuery('.full-screen-media-slider').slick('slickNext');
    })

    // copy below code into theme
    // expertise slider
    // slider settings
    jQuery('.full-screen-media-slider').slick({
      slidesToShow: 1,
      autoplay: false,
      dots: true,
      arrows: false,
      // prevArrow: true,
      // nextArrow: true,
      slidesToScroll: 1,
      infinite: true,
      fade: true,
      cssEase: 'linear'
    });
    
  });
</script>

<header class="has-bg-media container-fluid">
	<div class="full-screen-media-slider" style="min-height: 100%;">
		<div class="slide">
			<div class="columns">
				<div class="column text-column justify-content-end">
					<span class="year">1993</span>
					<span class="h1">land rover<br />defender puma</span>

					<div class="buttons">
						<a class="button button--icon" href="#">
							Meer lezen<i class="fa-solid fa-arrow-right" />
						</a>
					</div>
				</div>
			</div>

			<div class="media">
				<img
					class=""
					src="../../../../static/placeholders/slider-image_01.png"
					alt="some header image"
				/>
				<div class="overlay" />
				<div class="media-gradient" />
			</div>
		</div>

		<div class="slide">
			<div class="columns">
				<div class="column text-column justify-content-end">
					<span class="year">1993</span>
					<span class="h1">land rover<br />defender puma</span>

					<div class="buttons">
						<a class="button button--icon" href="#">
							Meer lezen<i class="fa-solid fa-arrow-right" />
						</a>
					</div>
				</div>
			</div>

			<div class="media">
				<img
					class=""
					src="../../../../static/placeholders/slider-image_01.png"
					alt="some header image"
				/>
				<div class="overlay" />
				<div class="media-gradient" />
			</div>
		</div>
	</div>
</header>

<style lang="scss" global>
	// slider styling
	.full-screen-media-slider {
		width: 100%;
		height: 100vh;
		min-height: 100vh;
		padding: 0;
		margin: 0;

		.bg-img {
			position: absolute;
			top: 0px;
			left: 0;
			width: 100%;
			height: 100vh;
			z-index: -20;

			object-fit: cover;
		}

		.slick-slide {
			position: relative;
			width: 100%;
			height: 100%;

			img {
				position: absolute;
				width: 100%;
				height: 100%;
				object-fit: cover;
			}

			video {
				position: absolute;
				display: block;
				width: 100%;
				height: 100%;
				object-fit: cover;
				object-position: center;
			}
		}

		.slick-track,
		.slick-list,
		.slick-slide {
			height: 100%;
			margin: 0;
		}

		.slick-dots {
			position: relative;
			display: block;

			top: -110px;
			z-index: 1;
			width: 100%;
			list-style: none;
			text-align: center;
			padding: 0;

			li {
				display: inline-block;
				height: 100%;
				margin: 0 4px;
				padding: 0;

				button {
					background: $white;
					height: 14px;
					width: 14px;
					overflow: hidden;
					border: none;
					outline: none;
					border-radius: 50px;
					line-height: 0;
					font-size: 0.5;
					color: transparent;

					&:hover {
						background-color: $blue;
						color: $blue;
						// outline: 3px solid $blue;
					}
				}

				&.slick-active {
					pointer-events: none;

					button {
						background: $blue;
						color: $blue;
						// outline-offset: 3px;
						// outline: 3px solid $blue;
					}
				}
			}
		}
	}

	// headert styling (overwrites some of full-screen-media-slider)
	header {
		position: relative;
		width: 100%;
		height: 100vh;
		display: flex;
		padding: 0 40px;
		padding-top: 148px;

		@include media-breakpoint-down(lg) {
			padding: 0;
			padding-top: 148px;
		}

		.overlay {
			position: absolute;
			width: 100%;
			height: 100%;
			top: 0;
			left: 0;
			background-color: rgba(10, 56, 79, 0.2);
			z-index: 1;
		}

		.columns {
			position: absolute;
			display: flex;
			flex-direction: row;
			margin: 30px 0;
			padding-bottom: 81px;
			padding-left: 50px;
			z-index: 999;

			@include media-breakpoint-down(lg) {
				flex-wrap: wrap;
				margin-bottom: 0;

				padding-left: 20px;
			}

			.column {
				position: relative;
				display: block;
				width: 100%;
				height: 100%;

				&.half-width {
					width: 70%;
				}

				&.text-column {
					display: flex;
					flex-direction: column;
					justify-content: center;

					@include media-breakpoint-down(lg) {
						padding-top: 0;
						margin-bottom: 40px;
						padding-left: 5px;
					}

					&.justify-content-end {
						padding: 46px 0;
					}

					h1,
					.h1 {
						width: 100%;
						text-transform: uppercase;
						color: $white;
						font-weight: 800;
						font-size: 4.4rem;
						line-height: 1;
						margin-bottom: 20px;

						@include media-breakpoint-down(lg) {
							width: 100%;
							font-size: 3rem;
						}
						@include media-breakpoint-down(md) {
							font-size: 2.4rem;
						}
					}

					.year {
						background: $black;
						position: relative;
						top: -12px;
						color: $white;
						font-weight: 600;
						font-size: 1.5rem;
						margin: 0;
						width: fit-content;
						padding: 3px 12px;

						@include media-breakpoint-down(lg) {
							font-size: 2rem;
						}
						@include media-breakpoint-down(md) {
							font-size: 1.4rem;
						}
					}

					// .button {
					//   margin-right: 20px;
					//   width: max-content;
					// }

					// .buttons {
					//   display: flex;
					//   width: max-content;
					//   margin-top: 10px;
					//   text-transform: none;
					//   z-index: 200;

					//   @include media-breakpoint-down(sm) {
					//     justify-content: center;
					//   }

					//   .button {
					//     background: $blue;
					//     padding: 0;
					//     margin-right: 0;

					//     &--content {
					//       padding: 0 15px;

					//     }

					//     &--icon {
					//       height: 100%;
					//       padding:0 17px;
					//       border-left: 1px solid rgb(77, 76, 76);
					//       display: flex;
					//       align-items: center;

					//       i {
					//         background: none;
					//         height: fit-content;
					//         padding: 5px 0 0 0;
					//         font-size: 1.5rem;
					//       }
					//     }

					//     &:hover {
					//       background: $blue;

					//        .button--icon {
					//         background: $light-blue;
					//         border-left: 1px solid $light-blue;

					//         i {
					//           background: none;
					//         }
					//       }

					//     }
					//   }
					// }
				}

				&.image-column {
					display: flex;
					width: 100%;
					height: 100%;
					align-items: center;
				}
			}
		}

		&.has-bg-media {
			min-height: 100vh;
			top: 0;
			left: 0;
			display: flex;
			align-items: flex-end;

			& > .full-screen-media-slider {
				.slide {
					height: 100vh;

					.columns {
						height: 100%;
					}

					.media {
						height: 100%;
					}
				}

				.nav-buttons {
					position: absolute;
					z-index: 1;
					bottom: 382px;
					left: 46px;

					@include media-breakpoint-down(lg) {
						width: fit-content;
						bottom: 310px;
						left: 20px;
					}

					.slider-nav-prev,
					.slider-nav-next {
						position: relative;

						i {
							color: $white;
							font-size: 3rem;
							font-weight: 100;

							&:hover {
								color: $blue;
							}
						}
					}
					.slider-nav-next {
						margin-left: 10px;
					}
				}

				.slick-dots {
					position: absolute;
					display: flex;
					padding-right: 40px;
					padding-top: 25px;
					z-index: 50;
					right: 0;
					bottom: 60px;
					width: max-content;
					align-items: flex-end;
					top: inherit;

					li {
						position: relative;
						z-index: 40;
						height: max-content;
					}
				}
			}

			.container-fluid {
				margin: 0;
				padding: 0;
				position: absolute;
				left: 0;
				top: 0;
			}

			.columns .text-column {
				h1 {
					color: $white;
				}

				h3 {
					color: $blue;
				}

				p {
					color: $white;
				}

				.button--ghost {
					color: $white;

					&:hover {
						color: $blue;
					}
				}
			}

			@include media-breakpoint-down(md) {
				.columns .column {
					&.text-column {
						width: 100%;

						p {
							margin-top: 20px;
							width: 70%;
						}

						.buttons {
							margin-top: 7px;
						}
					}
				}
			}
		}
	}

	.media-gradient {
		&::before {
			content: '';
			width: 100%;
			height: 40%;
			position: absolute;
			top: 0;
			left: 0;
			z-index: 50;
			background: rgb(2, 12, 28);
			background: linear-gradient(180deg, rgba(2, 12, 28, 1) 0%, rgba(2, 12, 28, 0) 100%);
		}

		&::after {
			content: '';
			// background: red;
			width: 100%;
			height: 30%;
			position: absolute;
			bottom: 0;
			left: 0;
			z-index: 50;

			background: rgb(2, 12, 28);
			background: linear-gradient(0deg, rgba(2, 12, 28, 1) 0%, rgba(2, 12, 28, 0) 100%);
		}
	}
</style>
