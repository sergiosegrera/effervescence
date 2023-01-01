<script>
	import picture1 from '../assets/picture1.webp';
	import picture2 from '../assets/picture2.webp';
	import picture3 from '../assets/picture3.webp';
	import picture4 from '../assets/picture4.webp';

	export let header = 'Gallery';
</script>

<div id="container">
	<h2>{header}</h2>
	<div id="images">
		<figure>
			<img src={picture1} alt="Night Crawler Cocktail" width="256" height="256" />
			<figcaption>Night Crawler</figcaption>
		</figure>
		<figure>
			<img src={picture2} alt="The Lounge" width="256" height="256" />
			<figcaption>The Lounge</figcaption>
		</figure>
		<figure>
			<img src={picture3} alt="The Jab Cocktail" width="256" height="256" />
			<figcaption>The Jab</figcaption>
		</figure>
		<figure>
			<img src={picture4} alt="The Twins" width="256" height="256" />
			<figcaption>The Twins</figcaption>
		</figure>
	</div>
</div>

<style>
	#container {
		max-width: 100vw;
		margin-top: 64px;
		margin-left: 32px;
		margin-bottom: 64px;
	}

	h2 {
		color: white;
		font-family: 'Caveat', cursive;
		font-size: 24px;
		margin-bottom: 16px;
	}

	#images {
		display: flex;
		overflow-x: scroll;
		overflow-y: hidden;
		gap: 16px;
		-ms-overflow-style: none;
		scrollbar-width: none;
	}

	#images::-webkit-scrollbar {
		display: none;
	}

	figure {
		width: 256px;
		height: 256px;
		min-width: 256px;
		min-height: 256px;
		border: 1px solid white;
	}

	figcaption {
		position: relative;
		z-index: 1;
		color: white;
		top: -48px;
		left: 16px;
	}

	@media (min-width: 768px) {
		#container {
			margin-left: 0px;
		}

		h2 {
			margin-left: 8px;
		}

		#images {
			gap: 64px;
		}
	}
</style>
