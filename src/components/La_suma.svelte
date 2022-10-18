<script>
	let count = 0;
	$: doubled = count * 2;
	$: numeroTela = count >= 5000 ? 'grande' : '' 

	function mais() {
		count += 1;
	}

	function menos() {
		count -= 1;
	}

	function zero() {
		count = 0;
	}

	function mais100() {
		count += 100;
	}

	function menos100() {
		count -= 100;
	}

</script>

<main class="background">
	<p class="text">
		Lhes apresento <strong class="laSuma">La Suma</strong>
	</p>

	<div class={`${numeroTela}`}>
		<h1 class="suma">
			{count} 
		</h1>

		<span class="dobro">
			{doubled}
		</span>
	</div>

	<div class="buttons">
		<button class="maisCem" on:click={mais100}>
			+100
		</button>

		<button class="menosCem" on:click={menos100}>
			-100
		</button>

		<button class="mais" on:click={mais}>
			+
		</button>

		<button class="zero" on:click={zero}>
			Zerar
		</button>

		<button class="menos" on:click={menos}>
			-
		</button>
	</div>
</main>

<style>
	.text {
		color: rgb(14, 24, 32);
		font-family: 'Comic Sans MS';
		font-SIZE: 2em;
		text-align: center;
	}

	.mais {
		color: rgb(14, 24, 32);
		font-size: 0.9rem;
		border-radius: 40%;
        border: 1px solid black;
        position: relative;
		left: 235px;
		bottom: 150px;
	}

	.menos {
		color: rgb(14, 24, 32);
		font-size: 0.9rem;
		border-radius: 40%;
        border: 1px solid black;
        position: relative;
		left: 275px;
		bottom: 150px;
	}

	.zero {
		border: 1px solid black;
		position: relative;
		left: 254px;
		bottom: 150px;
	}

	.suma {
		font-size: 6em;
		position: relative;
		left: 168px;
		color: rgb(14, 24, 32);
	}

	.laSuma {
		text-decoration: underline;
	}

	.dobro {
		font-size: 6em;
		position: relative;
		left: 568px;
		bottom: 170px;
		color: rgb(14, 24, 32);
	}

	.maisCem {
		position: relative;
		left: 275px;
		bottom: 150px;
	}

	.menosCem {
		position: relative;
		left: 445px;
		bottom: 150px;
	}

	.buttons {
		position: relative;
		left: -15px
	}

	.grande {
		position: relative;
		left: -100px;
	}

	.background {
		background-color: white;
	}
</style>