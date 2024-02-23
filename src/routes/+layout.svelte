<script>
	import Footer from "$lib/components/Footer.svelte";
import "./styles.css";
</script>

<div class="app">
	<h1 class="call-to-action">Ethan & Shelby's Commitment Ceremony</h1>
	<main>
		<slot />
	</main>

	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		align-items: center;
		min-height: 100vh;
	}

	.call-to-action {
		font-size: 2.5rem;
		text-align: right;
		margin: 0;
		padding: 2rem;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 70rem;
		margin: 0 auto;
		box-sizing: border-box;
		position: relative;
	}
</style>
