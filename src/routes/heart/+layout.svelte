<script lang="ts">
</script>

<div class="submenu">
	<aside>
		<nav>
			<ul>
				<li><a href="/heart">Game Home</a></li>
			</ul>
		</nav>
	</aside>
	<main>
		<slot />
	</main>
</div>
<footer>
	Buy the game <a
		href="https://rowanrookanddecard.com/product-category/game-systems/resistance/heart/">here</a
	>!
</footer>

<style>
	.submenu {
		display: grid;
		grid-template-columns: 200px 60ch;
	}
</style>
