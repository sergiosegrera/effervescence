<script>
	// @ts-nocheck
	import marker from '../assets/marker.svg';
	import { onMount } from 'svelte';

	let container;
	let map;
	let zoom = 14;
	let center = { lat: 45.4619, lng: -73.5671 };

	onMount(() => {
		map = new google.maps.Map(container, {
			zoom,
			center,
			mapId: 'e53247aa11b71a0d'
		});

		new google.maps.Marker({
			position: center,
			map,
			title: 'Effervescence',
			icon: marker
		});
	});
</script>

<svelte:head>
	<!-- Google Maps API -->
	<script
		defer
		async
		src="https://maps.googleapis.com/maps/api/js?key=AIzaSyCL2sp6thxEmtAjTbftbJRcjxoR4q5cJrs"
	></script>
</svelte:head>

<div bind:this={container} />

<style>
	div {
		height: 160px;
	}
</style>
