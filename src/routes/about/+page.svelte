<script>
	// Definisanje promenljive 'listaZadataka' koja će sadržavati zadatke
	let listaZadataka = ['Zadatak 1', 'Zadatak 2', 'Zadatak 3'];

	// Funkcija za dodavanje novog zadatka u listu
	function dodajZadatak() {
		// Prompt korisnika za unos novog zadatka
		const noviZadatak = prompt('Unesite novi zadatak:');

		// Provera da li je korisnik unio neki tekst
		if (noviZadatak) {
			// Ažuriranje 'listaZadataka' dodavanjem novog zadatka
			listaZadataka = [...listaZadataka, noviZadatak];
		}
	}

	// Funkcija za uklanjanje zadatka iz liste
	function ukloniZadatak(index) {
		// Filtriranje 'listaZadataka' da ukloni zadatak sa određenim indeksom
		listaZadataka = listaZadataka.filter((_, i) => i !== index);
	}
</script>

<main>
	<!-- Naslov stranice -->
	<h1>Lista Zadataka</h1>

	<!-- Lista za prikazivanje zadataka -->
	<ul>
		<!-- Svelteova direktiva `{#each}` omogućava iteraciju kroz niz -->
		{#each listaZadataka as zadatak, index (zadatak)}
			<!-- Elementi koji prikazuju svaki zadatak u listi -->
			<!-- Kada korisnik klikne na zadatak, poziva se funkcija 'ukloniZadatak' sa odgovarajućim indeksom -->
			<li on:click={() => ukloniZadatak(index)}>{zadatak}</li>
		{/each}
	</ul>

	<!-- Dugme koje poziva funkciju za dodavanje novog zadatka -->
	<button on:click={dodajZadatak}>Dodaj zadatak</button>
</main>

<style>
	/* Stilizacija za bolji izgled */
	ul {
		border: 2px solid;
		list-style-type: none;
		padding: 0;
	}

	li {
		border: 1px solid;
		cursor: pointer;
		margin-bottom: 5px;
	}
</style>
