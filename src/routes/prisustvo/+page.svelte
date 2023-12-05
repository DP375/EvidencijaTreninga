<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>


<script>
  const buttonClickHandler = () => {
    window.location.replace('http://localhost:5174/vx');
  };
</script>


<div class="text-column">
	
	<h1>h1</h1>

	<p>
		<a href="https://kit.svelte.dev">SvelteKit</a> linkovanje
	</p>

	



	<pre>ovde pišem mrtvi HTML</pre>
	<button id= mau on:click={buttonClickHandler} >tajmer</button> >
	<button id=clanarine >gumbZaClanarine</button>

	
	
</div>
	
<style>
    #mau {
        font-size: 1.4em;
        width: 6em;
        height: 6em;
        border-radius: 50%;
        background: radial-gradient(circle at 25% 25%, hsl(210, 40%, 80%) 0, hsl(210, 30%, 70%) 100%);
        box-shadow: 0 8px 0 hsl(210, 20%, 60%), 2px 12px 10px rgba(0, 0, 0, .35);
        color: hsl(210, 20%, 60%);
        text-shadow: -1px -1px 2px rgba(0, 0, 0, 0.3), 1px 1px 2px rgba(255, 255, 255, 0.4);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        transform: translate(0, -8px);
        transition: all 0.2s;
    }

    #mau:active {
        transform: translate(0, -2px);
        box-shadow: 0 2px 0 hsl(210, 20%, 60%), 2px 6px 10px rgba(0, 0, 0, .35);
    }


	#clanarine {
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