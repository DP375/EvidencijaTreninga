<script>
	let name = '';
	let surname = '';
	let pretraga = '';
	let listaClanova = [
		{ ime: 'Ana', prezime: 'Anić' },
		{ ime: 'Marko', prezime: 'Marković' },
		{ ime: 'Jovana', prezime: 'Jovanović' }
	];

	function dodajClana() {
		if (name && surname) {
			listaClanova = [...listaClanova, { ime: name, prezime: surname }];
			// Resetuj polja nakon dodavanja člana
			name = '';
			surname = '';
			drugaAkcija();
		}
	}

	function drugaAkcija() {
		console.log('druga akcija');
		alert('dodao si clana');
	}
</script>

<main>
	<input bind:value={name} placeholder="unesi ime" />
	<input bind:value={surname} placeholder="unesi prezime" />

	<button on:click={dodajClana}>Dodaj člana</button>

	<h1>Hello {name + ' ' + surname}!</h1>

	<div>
		<input bind:value={pretraga} placeholder="Pretraži članove" />
		<h2>Lista članova</h2>

		<ul>
			{#each listaClanova.filter((clan) => clan.ime
						.toLowerCase()
						.includes(pretraga.toLowerCase()) || clan.prezime
						.toLowerCase()
						.includes(pretraga.toLowerCase())) as clan (clan.ime + clan.prezime)}
				<li>{clan.ime} {clan.prezime}</li>
			{/each}
		</ul>
	</div>
</main>

<style>
	ul {
		border: 2px solid;
		list-style-type: none;
		padding: 0;
	}

	li {
		border: 1px solid;
		margin-bottom: 10px;
	}
</style>
