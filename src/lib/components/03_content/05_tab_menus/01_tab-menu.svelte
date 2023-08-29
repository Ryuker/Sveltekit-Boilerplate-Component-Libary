<script>
	/* Basic Tab menu -  
    - lising of tabs on the left side
    - opens and closes content on the right side as tab is clicked on
    - uses jQuery to assign and unassign classes
		- doesn't support mobile rez

    author: Joeri van Ees 
  */

	import { onMount } from 'svelte';
	import jQuery from 'jquery/dist/jquery';


  onMount(async () => {
	// const module = await import('slick-carousel');    // import jquery

		jQuery(document).ready(function () {
			tab_toggle();
		});

		function tab_toggle() {
			jQuery('body').on('click', '.tab-toggle', function (event) {
				event.preventDefault();
				jQuery('.tab-toggle').removeClass('open');
				jQuery('.tab__content').removeClass('open');
				var tab_id = jQuery(this).data('toggle');
				jQuery(this).addClass('open');
				jQuery('#' + tab_id).addClass('open');
			});
		}
  });
</script>

<h1>basic tab menu component</h1>

<section class="tab-content">
	<div class="container">
		<div class="tabs tabs--vertical">
			<div class="tabs_titles">
				<ul>
					<li>
						<a class="tab-toggle open" data-toggle="tab-1" href="/comp-builder"
							>Constructieve thermische ontkoppeling</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-2" href="/comp-builder">Woningconcepten</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-3" href="/comp-builder">Deuveltechniek</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-4" href="/comp-builder">Luchtdicht bouwen</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-5" href="/comp-builder">Dilatatiesystemen</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-6" href="/comp-builder">Bouwakoestiek 6</a>
					</li>
					<li>
						<a class="tab-toggle" data-toggle="tab-7" href="/comp-builder">Ruimteakoestiek</a>
					</li>
				</ul>
			</div>

			<div class="tabs__content">
				<div id="tab-1" class="tab__content open" data-tab="1">
					<h3 class="h2">Safe. Secure.</h3>
					<p>
						Bij Navacqs staan we voor zekerheid en veiligheid op ieder vlak. Al onze producten
						zorgen voor extra veiligheid en zekerheid bij iedere specialistische toepassing. Ook de
						website en andere data worden extra veilig binnen Europa gehost. Zo houden u en Navacqs
						de controle in handen en wordt niets aan het toeval overgelaten.
					</p>
				</div>

				<div id="tab-2" class="tab__content" data-tab="2">
					<h3 class="h2">Betrouwbaar. Snel.</h3>
					<p>
						Dankzij de strategisch centrale voorraadlocatie in Rotterdam worden pakketten en pallets
						veilig en zeker vervoerd met gerenommeerde partijen. Eén van deze partijen is UPS.
						Iedere zending wordt voorzien van een unieke Track &amp; Trace code zodat uw zending op
						ieder moment te traceren is. Omdat ieder product bij ons op voorraad ligt worden
						bestellingen op werkdagen voor 16:00 geplaatst de volgende werkdag al bezorgd!
					</p>
				</div>

				<div id="tab-3" class="tab__content" data-tab="3">
					<h3 class="h2">24/7. Bereikbaar.</h3>
					<p>
						Wij zijn altijd bereikbaar! Met het geavanceerde en veilige online platform
						www.www.navacqs.nl wordt het eenvoudig om 24/7 een product te vinden voor uw
						specialistische toepassing. Ook zijn wij bij Navacqs gewoon nog bereikbaar op een manier
						zoals u wellicht wenst, namelijk telefonisch, per e-mail, per fax of zelfs per
						post(duif).
					</p>
				</div>
				<div id="tab-4" class="tab__content" data-tab="4">
					<h3 class="h2">Rotterdam. Nederland.</h3>
					<p>
						Met onze strategische locatie in Rotterdam kan Navacqs naast Nederland ook klanten in
						omliggende landen optimaal bedienen. Door nauwe samenwerkingen en ervaringen kunnen we
						onze kennis en expertise overbrengen op de gehele Europese markt. Iedere markt vereist
						een specialistische aanpak en vraagt om doordachte oplossingen per toepassing.
					</p>
				</div>
				<div id="tab-5" class="tab__content" data-tab="5">
					<h3 class="h2">Tevredenheid. Waardering.</h3>
					<p>
						Wij streven naar optimale klanttevredenheid. Door te luisteren naar u als klant en de
						processen hierop aan te passen zorgen wij voor de hoogst haalbare waardering. Het
						Navacqs team zet altijd dat extra stapje om u zo optimaal mogelijk van dienst te zijn
						bij het vinden van het juiste veiligheidsproduct en toepassing.
					</p>
				</div>
				<div id="tab-6" class="tab__content" data-tab="6">
					<h3 class="h2">Vivamus. Elementum.</h3>
					<p>
						Nullam elementum nibh a varius aliquam. Mauris ut dignissim arcu. Vivamus arcu neque, imperdiet non metus accumsan, ultricies sollicitudin lorem.
					</p>
				</div>
				<div id="tab-7" class="tab__content" data-tab="7">
					<h3 class="h2">Lorem ipsum. Fusce justo.</h3>
					<p>
						Fusce justo nunc, vulputate non neque nec, eleifend ultricies nunc. Vivamus tortor enim, lobortis in erat nec, luctus euismod nibh. Donec et molestie mauris. Pellentesque pellentesque sodales orci, pellentesque aliquet dui pretium quis. Suspendisse elementum egestas suscipit.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	.tab-content {
		// background: rgb(232, 94, 94);
		width: 100%;
		display: flex;
		flex-direction: row;

		position: relative;
		padding-top: 60px;
		padding-bottom: 60px;

		.tabs {
			display: flex;

			@include media-breakpoint-down(sm) {
				display: none;
			}

			&--vertical {
				// display: flex;

				@include media-breakpoint-down(sm) {
					display: none;
				}
			}

			.tabs_titles {
				position: relative;
				background: rgb(95, 95, 173);
				display: flex;

				border: none;
				min-width: 33%;

				ul {
					// background: $secondary;
					display: block;
					width: 100%;
					list-style: none;

					li {
						border-bottom: 1px solid rgb(58, 58, 102);
						a {
							padding: 10px;
							display: block;
							color: white;
							text-decoration: none;

							&.open,
							&:hover {
								background: rgb(127, 127, 205);
								display: block;
								max-height: auto;
							}
						}
					}
				}

				.tabs__title {
					padding: 16px 24px;
					border: none;
					margin: 0;

					&--has-arrow {
						display: flex;
						align-items: center;
						justify-content: space-between;
					}
				}

				label {
					background: #45ac34;
					color: white;
					font-weight: 700;
					display: block;
					margin-bottom: 0.45em;
				}
			}
			.tabs__content {
				display: flex;
				position: relative;
				width: 100%;
				background: #f4f5f9;
				padding: 28px;

				.tab__content {
					display: none;

					&.open {
						display: block;
					}
				}
			}
		}
	}
</style>
