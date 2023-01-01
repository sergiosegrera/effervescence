<script>
	import facebook from '../assets/facebook.svg';
	import instagram from '../assets/instagram.svg';
</script>

<footer>
	<a href="https://sergiosegrera.com">Segrera Design</a>
	<div>
		<a href="https://facebook.com"><img alt="Facebook" src={facebook} width="24" height="24" /></a>
		<a href="https://instagram.com"
			><img alt="Instagram" src={instagram} width="24" height="24" /></a
		>
	</div>
</footer>

<style>
	footer {
		display: flex;
		align-items: center;
		justify-content: space-between;
		margin: 32px;
	}

	a {
		color: white;
		font-size: 8px;
		text-decoration: none;
	}

	div {
		display: flex;
		gap: 12px;
	}

	@media (min-width: 768px) {
		footer {
			flex-direction: column;
			justify-content: center;
			gap: 48px;
		}

		a {
			order: 2;
		}

		div {
			gap: 16px;
		}
	}
</style>
