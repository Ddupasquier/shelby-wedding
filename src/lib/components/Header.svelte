<script>
	import { page } from "$app/stores";
</script>

<header>
	<div class="corner">
		<!-- <a href="https://kit.svelte.dev">
			<img src={logo} alt="SvelteKit" />
		</a> -->
	</div>

	<nav>
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg> -->
		<!-- <ul>
			<li aria-current={$page.url.pathname === "/" ? "page" : undefined}>
				<a href="/">RSVP</a>
			</li>
			<li
				aria-current={$page.url.pathname === "/where"
					? "page"
					: undefined}
			>
				<a href="/where">Where</a>
			</li>
			<li
				aria-current={$page.url.pathname === "/pics"
					? "page"
					: undefined}
			>
				<a href="/pics">Pics</a>
			</li>
		</ul> -->
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg> -->
	</nav>

	<div class="corner">
		<!-- <a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" />
		</a> -->
	</div>
</header>

<style>
	header {
		position: fixed;
		width: 100%;
		display: flex;
		justify-content: space-between;
		background: black;
		color: white;
		z-index: 1000;
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background-size: contain;
		color: white;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current="page"]::before {
		--size: 6px;
		content: "";
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--sandstone);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: white;
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
