<script>
	const buttonClickTimer = () => {
		window.location.replace('http://localhost:5174/vx');
	};

	const buttonClickClanarina = () => {
		window.location.replace('http://localhost:5174/clanarine');
	};

	const buttonClickPrisustvo = () => {
		window.location.replace('http://localhost:5174/prisustvo');
	};

	const buttonClickBeleske = () => {
		window.location.replace('http://localhost:5174/biljeznica');
	};

	const buttonClickClanovi = () => {
		window.location.replace('http://localhost:5174/clanovi');
	};
</script>

<svelte:head>
	<title>Raskrizje</title>
</svelte:head>

<div>
	<button id="mau" on:click={buttonClickTimer}>tajmer</button>
	<button on:click={buttonClickClanarina}>Članarine</button>
	<button on:click={buttonClickPrisustvo}>Prisustvo</button>
	<button on:click={buttonClickClanovi}>Članovi</button>
	<button on:click={buttonClickBeleske}>Beleške</button>
</div>

<style>
	#mau {
		font-size: 1.4em;
		width: 6em;
		height: 6em;
		border-radius: 50%;
		background: radial-gradient(circle at 25% 25%, hsl(210, 40%, 80%) 0, hsl(210, 30%, 70%) 100%);
		box-shadow:
			0 8px 0 hsl(210, 20%, 60%),
			2px 12px 10px rgba(0, 0, 0, 0.35);
		color: hsl(210, 20%, 60%);
		text-shadow:
			-1px -1px 2px rgba(0, 0, 0, 0.3),
			1px 1px 2px rgba(255, 255, 255, 0.4);
		text-transform: uppercase;
		letter-spacing: 0.05em;
		transform: translate(0, -8px);
		transition: all 0.2s;
	}

	#mau:active {
		transform: translate(0, -2px);
		box-shadow:
			0 2px 0 hsl(210, 20%, 60%),
			2px 6px 10px rgba(0, 0, 0, 0.35);
	}

	button {
		background-color: #007bff;
		border-color: #007bff;
		color: #fff;
		padding: 0.5rem 1rem;
		font-size: 1rem;
		line-height: 1.5;
		border-radius: 0.25rem;
		cursor: pointer;
	}
</style>
