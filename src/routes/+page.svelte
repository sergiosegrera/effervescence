<script>
	import Carousel from '../lib/carousel.svelte';
	import Map from '../lib/map.svelte';

	import menu from '../assets/menu.pdf';
	import welcome from '../assets/welcome.svg';
</script>

<section id="top">
	<section id="menu">
		<a href={menu}>Drink Menu</a>
	</section>
	<section id="carousel">
		<Carousel />
	</section>
	<section id="intro">
		<img alt="Welcome to Effervescence" src={welcome} width="196" height="56" />
		<p>
			The premier cocktail club for the discerning drinker. Here at Effervescence, we take our
			cocktails seriously, crafting unique and delicious beverages that will tantalize your taste
			buds and elevate your evening.
		</p>
		<p>
			Our dimly-lit lounge sets the stage for a sophisticated and mysterious atmosphere, inviting
			you to unwind and let go of your inhibitions.
		</p>
		<p>Come join us at Effervescence and discover the magic of the perfect cocktail.</p>
	</section>
</section>
<section id="bottom">
	<section id="hours">
		<h2>Hours</h2>
		<ul>
			<li>
				<strong>Sun - Wed</strong>
				<div />
				<span>8pm - 1am</span>
			</li>
			<li>
				<strong>Thu - Sat</strong>
				<div />
				<span>6pm - 3am</span>
			</li>
		</ul>
	</section>
	<section id="location">
		<h2>Location</h2>
		<address>
			1000 Rue Wellington<br />Verdun, Montreal<br /><a href="mailto:contact@effervescence.ca"
				>contact@effervescence.ca</a
			><br /><a href="tel:1-514-222-2518">(514) 222 5020</a>
		</address>
	</section>
	<section id="map">
		<Map />
	</section>
</section>

<style>
	#menu {
		display: flex;
		justify-content: center;
		margin-top: 256px;
		margin-left: 32px;
		margin-right: 32px;
		margin-bottom: 256px;
	}
	#menu a {
		font-family: 'Caveat', sans-serif;
		font-size: 32px;
		text-decoration: none;
		color: white;
		padding-top: 16px;
		padding-left: 24px;
		padding-right: 24px;
		padding-bottom: 16px;
		border: 1px solid white;
		font-weight: normal;
	}
	#menu a:hover {
		transform: scale(1.01);
	}
	#intro {
		font-size: 18px;
		margin-left: 32px;
		margin-right: 32px;
	}
	#intro img {
		margin-bottom: 24px;
	}
	#bottom {
		margin-top: 48px;
		margin-bottom: 48px;
	}
	#hours {
		margin-left: 32px;
		margin-right: 32px;
	}
	#hours ul {
		list-style: none;
		line-height: 1.75;
	}
	#hours ul li {
		color: white;
		display: flex;
		justify-content: space-between;
		align-items: baseline;
	}
	#hours ul li div {
		flex-grow: 1;
		border-bottom-width: 1px;
		border-bottom-color: white;
		border-bottom-style: dashed;
		margin-left: 8px;
		margin-right: 8px;
	}
	#hours ul li strong {
		font-weight: 700;
	}
	#location {
		margin-top: 48px;
		margin-left: 32px;
		margin-right: 32px;
	}
	address {
		font-size: 16px;
		color: white;
		font-style: normal;
		line-height: 1.75;
	}
	address a {
		color: white;
		text-decoration: underline;
	}
	p {
		text-align: justify;
		color: white;
		margin-bottom: 12px;
	}
	h2 {
		font-family: 'Caveat', cursive;
		color: white;
		margin-bottom: 16px;
		font-size: 24px;
		font-weight: 500;
	}
	#map {
		width: 100vw;
		margin-top: 48px;
		object-fit: contain;
		place-self: center;
		align-self: center;
	}
	@media (min-width: 768px) {
		#top {
			display: grid;
			grid-template-columns: 1fr 1fr;
			grid-template-rows: 1fr auto;
			grid-template-areas:
				'a b'
				'c c';
			justify-items: center;
			align-items: center;
		}

		#menu {
			grid-area: a;
		}

		#carousel {
			grid-area: c;
		}

		#intro {
			grid-area: b;
			max-width: 800px;
		}

		#bottom {
			display: grid;
			grid-template-columns: 1fr 1fr;
			grid-template-rows: 1fr auto;
			grid-template-areas:
				'a b'
				'c c';
			max-width: 800px;
			margin-left: auto;
			margin-right: auto;
			margin-bottom: 64px;
		}

		#hours {
			grid-area: b;
		}

		#location {
			grid-area: a;
			margin-top: 0px;
		}

		#map {
			grid-area: c;
			max-width: 768px;
		}
	}
</style>
