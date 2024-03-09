<script lang="ts">
	let hitDice = 1;
	let name = '';
	let hitProtection = 0;
	let threat = 0;
	let movementFt = 0;
	let movementDice = 0;
	let ascendAC = 10;
	let descendAC = 0;
	let alignment = '';
	const specialAbilities = [];
	let attacks = '';
	let morale = 0;

	function convert() {
		hitProtection = hitDice * Math.floor(0.5 * ascendAC);
		movementDice = Math.floor(movementFt / 20);
		if (hitDice <= 10) {
			threat = hitDice;
		} else if (Math.floor(hitProtection / 12) <= 10) {
			threat = Math.floor(hitProtection / 12);
		} else {
			threat = 10;
		}
	}
</script>

<h1>NPC Converter</h1>
<body class="grid colums">
	<main>
		<form>
			<label>Name<input type="text" bind:value={name} placeholder="Name" /></label>
			<fieldset role="group">
				<label>Hit Dice<input type="number" bind:value={hitDice} /></label>
				<label>Armor Class<input type="number" bind:value={ascendAC} /></label>
				<label>Movement<input type="number" bind:value={movementFt} /></label>
			</fieldset>
			<fieldset>
				<label>Attacks<input type="text" bind:value={attacks} /></label>
			</fieldset>
			<fieldset>
				<label>Morale<input type="number" bind:value={morale} /></label>
				<select name="alignment" aria-label="Alignment" bind:value={alignment}>
					<option selected disabled>Pick Alignment</option>
					<option>Lawful</option>
					<option>Neutral</option>
					<option>Chaotic</option>
				</select>
			</fieldset>
			<button type="submit" on:click={convert}>Convert</button>
		</form>
	</main>
	<article>
		<header>{name}</header>
		<p>
			Threat {threat}, HP {hitProtection}, ATT {attacks}, MV {movementDice}, ML {morale}, AL
			<i>{alignment}</i>
		</p>
		<br />
		<p></p>
	</article>
</body>

<style>
	h1 {
		font-family: Baldur;
	}
	article {
		width: max-content;
	}
</style>
