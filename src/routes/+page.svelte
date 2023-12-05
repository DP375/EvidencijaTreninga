<script>
	import Counter from './Counter.svelte';
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Stoperica from './StopWatch.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h2>
		<h3>upravo to i radim braćo! Mučite se sa zadovoljstvom i Sizif je srećan</h3>
	</h2>
	<Stoperica />
	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h3 {
		width: 100%;
	}
</style>
