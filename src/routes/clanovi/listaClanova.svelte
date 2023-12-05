<!-- <script>
	let pretraga = '';
	let listaClanova = [
		{ ime: 'Ana', prezime: 'Anić' },
		{ ime: 'Marko', prezime: 'Marković' },
		{ ime: 'Jovana', prezime: 'Jovanović' }
	];
</script>

<input bind:value={pretraga} placeholder="pretrazi clanove" />
<h2>Lista clanova</h2>

<ul>
	{#each listaClanova as clan (clan.ime + clan.prezime)}
		<li>{clan.ime} {clan.prezime}</li>
	{/each}
</ul>

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
</style> -->
