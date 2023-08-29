<script>
	/* Fancybox Gallery
    - Images layed out in a grid
		- on click/tap opens lightbox with gallery
		- uses data-fancybox to add to the page lightbox

    - used on vanstooten.nl

    author: Joeri van Ees - created: 10/08/2022
  */
</script>

<section class="container content">
	<div class="container__header">
		<h1>Gallery</h1>
	</div>

	<div class="row gx-5 mt-2 mb-4">
		<div class="col-12 col-lg-12 images">
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&2/">
				<figure>
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&2/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&3/">
				<figure class="img-small">
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&3/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&4/">
				<figure class="img-small">
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&4/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&5/">
				<figure class="img-small">
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&5/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&6/">
				<figure class="img-small">
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&6/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&7/">
				<figure>
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&8/" />
				</figure>
			</a>
			<a data-fancybox="gallery" href="https://source.unsplash.com/random/300×300/?engine&9/">
				<figure>
					<img data-fancybox="part" src="https://source.unsplash.com/random/300×300/?engine&9/" />
				</figure>
			</a>
		</div>
	</div>
</section>

<style lang="scss" global>
	// gallery stylesheet
	@import '../../static/vendors/fancyapps/fancyapp';

		// optional column and image styling
	.container {
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 1400px;
		padding: 20px 40px 0;
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

	.images {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: space-between;

		@include media-breakpoint-down(lg) {
			margin-top: 30px;
		}

		a {
			display: contents;
		}

		.img-small {
			position: relative;
			height: 0;
			width: 47%;
			padding-bottom: 64.75%;
			margin-bottom: 30px;

			@include media-breakpoint-down(lg) {
				width: 48%;
			}

			img {
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				-o-object-fit: cover;
				object-fit: cover;
				-o-object-position: center;
				object-position: center;
			}
		}
	}
</style>
