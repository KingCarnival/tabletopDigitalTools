<script lang="ts">
	import '@picocss/pico';
	import '../app.css';
	import { fade } from 'svelte/transition';

	export let data;
</script>

<main>
	<div>
		{#key data.url}
			<div in:fade={{ duration: 300, delay: 300 }} out:fade={{ duration: 300 }}>
				<nav>
					<ul>
						<li><a href="/">Home</a></li>
						<li><a href="/">About</a></li>
					</ul>
					<ul>
						<li>
							<details class="dropdown">
								<summary>Games</summary>
								<ul dir="rtl">
									<li><a href="/errant">Errant</a></li>
									<li><a href="/fathom">Fathom</a></li>
									<li><a href="/hard-wired-island">Hard Wired Island</a></li>
									<li><a href="/heart">Heart: The City Beneath</a></li>
								</ul>
							</details>
						</li>
					</ul>
				</nav>
				<slot />
			</div>
		{/key}
	</div>
</main>
