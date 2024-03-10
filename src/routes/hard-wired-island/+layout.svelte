<script lang="ts">
</script>

<div class="submenu">
	<aside>
		<nav>
			<ul>
				<li><a href="/hard-wired-island">Game Home</a></li>
			</ul>
		</nav>
	</aside>
	<main>
		<slot />
	</main>
</div>
<footer>
	Buy the game <a href="https://ettin.itch.io/hard-wired-island">here</a>!
</footer>

<style>
	.submenu {
		display: grid;
		grid-template-columns: 200px 60ch;
	}

	nav {
		font-family: 'Big Shoulders Stencil Display', sans-serif;
		font-variation-settings: 'wght' 800;
	}
</style>
