<script lang="ts">
</script>

<div class="submenu">
	<aside>
		<nav>
			<ul>
				<li><a href="/fathom">Game Home</a></li>
			</ul>
		</nav>
	</aside>
	<main>
		<slot />
	</main>
</div>
<footer>
	Buy the game <a href="https://sulcata.itch.io/fathom">here</a>!
</footer>

<style>
	.submenu {
		display: grid;
		grid-template-columns: 200px 60ch;
	}
</style>
