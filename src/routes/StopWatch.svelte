<script>
	let startTime = 0;
	let running = false;
	let elapsedTime = 0;

	function startStopwatch() {
		if (!running) {
			startTime = new Date().getTime();
			running = true;
			updateElapsedTime();
		}
	}

	function stopStopwatch() {
		if (running) {
			running = false;
		}
	}

	function resetStopwatch() {
		if (!running) {
			startTime = 0;
			elapsedTime = 0;
		}
	}

	function updateElapsedTime() {
		if (running) {
			const currentTime = new Date().getTime();
			elapsedTime = currentTime - startTime;

			// Update every 100 milliseconds
			setTimeout(updateElapsedTime, 100);
		}
	}
</script>

<div>
	<div id="elapsedTime">
		Elapsed Time: {Math.floor(elapsedTime / 1000)} seconds {elapsedTime % 1000} milliseconds
	</div>
	<div id="buttons">
		<button on:click={startStopwatch} id="start-button">Start</button>
		<button on:click={stopStopwatch}>Stop</button>
		<button on:click={resetStopwatch}>Reset</button>
	</div>
</div>

<style>
	#elapsedTime {
		font-size: 24px;
		margin-bottom: 20px;
	}

	#buttons {
		margin-top: 10px;
		padding: 10px 20px;
		cursor: pointer;
		font-size: 16px;
	}

	#start-button:active {
		background-color: #000000;
	}
</style>
