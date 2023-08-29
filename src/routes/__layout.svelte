<script>
	import '../../node_modules/bootstrap/scss/bootstrap.scss';
	import '../app.scss';
	
	import Header from '$lib/header.svelte';
	import Nav from '$lib/nav.svelte';
</script>

<Header  />

<Nav />

<main>
	<slot  />
</main>

<footer><h3>Layout Footer</h3></footer>

<style lang="scss">
	@import '../scss/_main';

	:global {
		html {
			font-family: Arial, Helvetica, sans-serif;
			height: 100%;

			body {
				height: 100%;
				margin: 0;
				padding: 0;
				display: block;
				width: 100%;

				#svelte {
					display: flex;
					flex-direction: column;
					height: 100%;
					margin: 0;
					padding: 0;
					padding: 0 20px;

					main {
						background-color: rgb(240, 245, 166);
						display: block;
						flex: 1;
						margin: 0;
						width: 100%;

						&.h4 {
								color: red;
								text-align: center;
						}
					}

					a:hover {
							color: rgb(167, 167, 167);
					}
				}
			}
		}
	}

	h2 {
		color: $my-sass-color;
	}

	

	footer {
		background-color: rgb(131, 207, 209);
		display: flex;
		font-weight: bold;
		width: 100%;
		padding: 5px 0px;
		justify-content: center;
	}
</style>
