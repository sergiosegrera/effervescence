<script>
	import logo from '../assets/logo-small.svg';

	import background from '../assets/background.webp';
</script>

<header>
	<img alt="Main Logo" src={logo} width="149" height="56" />
	<a href="/fr">FR</a>
</header>
<div>
	<img id="background" src={background} alt="Background" width="768" height="900" />
</div>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 32px;
	}

	a,
	a:visited {
		font-family: 'Caveat', cursive;
		color: white;
		text-decoration: none;
	}

	div {
		display: flex;
		width: 100vw;
		overflow: hidden;
		justify-content: center;
		align-items: center;
		position: absolute;
		left: 0;
		top: 0;
		z-index: -1;
		animation: fade-in 3s;
	}
</style>
