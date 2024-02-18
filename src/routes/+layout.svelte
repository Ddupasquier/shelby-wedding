<script>
	import Footer from "$lib/components/Footer.svelte";
	import Header from "../lib/components/Header.svelte";
	import "./styles.css";
</script>

<div class="app">
	<div class="main-bg"></div>
	<div class="gradient"></div>

	<Header />

	<main>
		<slot />
		<div class="spacer"></div>
	</main>

	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	.main-bg {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-image: url("src/lib/images/space.jpg");
		background-size: cover;
		background-position: center center;
		background-repeat: no-repeat;
		z-index: -1;
	}

	.gradient {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background: radial-gradient(
			circle at 50% 80%,
			var(--moab-orange) 0%,
			/* Innermost color: sun color */ var(--sandstone) 40%,
			/* Second color: inner glow of the sunset */ var(--dark-green) 60%,
			/* Third color: outer glow of the sunset */ transparent 100%
				/* Transition to transparent to reveal the image */
		);
		z-index: 0; /* Overlay on top of the background image, under the content */
	}

	.spacer {
		height: 10rem;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		padding-top: 5rem;
		width: 100%;
		max-width: 70rem;
		margin: 0 auto;
		box-sizing: border-box;
		position: relative;
		z-index: 2;
	}
</style>
