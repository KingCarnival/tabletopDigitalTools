<script lang="ts">
</script>

<div class="submenu">
	<aside>
		<nav>
			<ul>
				<li><a href="/errant">Game Home</a></li>
				<li><a href="/errant/npc-converter">NPC Converter</a></li>
			</ul>
		</nav>
	</aside>
	<main>
		<slot />
	</main>
</div>
<footer>
	Buy the game here: <a href="https://killjestergames.itch.io/errant">digital</a> and
	<a href="https://www.killjester.com/products/errantorder">physically</a>!
</footer>

<style>
	.submenu {
		display: grid;
		grid-template-columns: 200px 60ch;
	}
</style>
