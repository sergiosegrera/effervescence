<script>
	import Top from '../lib/top.svelte';
	import Bottom from '../lib/bottom.svelte';
</script>

<svelte:head>
	<!-- Google tag (gtag.js) -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=G-Y93WTD4WF5"></script>
	<script>
		window.dataLayer = window.dataLayer || [];
		function gtag() {
			dataLayer.push(arguments);
		}
		gtag('js', new Date());

		gtag('config', 'G-Y93WTD4WF5');
	</script>
</svelte:head>

<Top />
<slot />
<Bottom />
