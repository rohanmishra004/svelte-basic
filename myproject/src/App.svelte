<script>
	let name = "Yoshi";
	let beltColor = "black";

	function changeBeltColor() {
		beltColor = beltColor === "black" ? "orange" : "black";
	}

	function handleInputBelt(e) {
		e.preventDefault();
		console.log(e.target.value);
		beltColor = e.target.value;
	}

	function handleInputName(e) {
		e.preventDefault();
		console.log(e.target.value);
		name = e.target.value;
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p style="color:{beltColor}">My Belt Color is {beltColor}</p>
	<button on:click={changeBeltColor}>Change</button>
	<input on:input={handleInputBelt} type="text" value={beltColor} />
	<input type="text" bind:value={name} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
