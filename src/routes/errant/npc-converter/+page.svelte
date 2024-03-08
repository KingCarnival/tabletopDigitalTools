<script lang="ts">
	let hitDice = 0;
	let name = '';
	let hitProtection = 0;
	let threat = 0;
	let movementFt = 0;
	let movementDice = 0;
	let ascendAC = 10;

	function convert() {
		hitProtection = hitDice * (0.5 * ascendAC);
		movementDice = movementFt / 20;
		if (hitDice <= 10) {
			threat = hitDice;
		} else if (hitProtection / 12 <= 10) {
			threat = hitProtection / 12;
		} else {
			threat = 10;
		}
	}
</script>

<h1>NPC Converter</h1>
<body>
	<form>
		<label>Name<input type="text" bind:value={name} placeholder="Name" /></label>
		<fieldset role="group">
			<label>Hit Dice<input type="number" bind:value={hitDice} placeholder="1" /></label>
			<label>Armor Class<input type="number" bind:value={ascendAC} placeholder="10" /></label>
			<label>Movement<input type="number" bind:value={movementFt} placeholder="20" /></label>
		</fieldset>
		<button type="submit" on:click={convert}>Convert</button>
	</form>
	<article>
		<header><h2>{name}</h2></header>
		<p>
			HP: {hitProtection}
			Threat: {threat}
			MV: {movementDice}
		</p>
	</article>
</body>

<style>
	h1 {
		font-family: Baldur;
	}
</style>
