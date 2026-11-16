<script lang="ts">
	import { browser } from '$app/env';

	let dark = $state(false);

	if (browser) {
		dark = document.body.getAttribute('data-theme') === 'dark';
	}

	$effect(() => {
		if (dark) {
			document.body.setAttribute('data-theme', 'dark');
		} else {
			document.body.setAttribute('data-theme', '');
		}
	});
</script>

<div class="sticky top-0 z-10">
	<nav class="p-4 my-4">
		<h5 class="link"><a href="/">ELLIE KULMBAK</a></h5>
		<div class="flex-1 justify-end flex gap-4">
			<h5 class="link"><a href="/about-me">ABOUT ME</a></h5>
			<h5 class="link"><a href="/projects">PROJECT</a></h5>
			<button onclick={() => (dark = !dark)}>Lights</button>
		</div>
	</nav>
</div>

<style lang="scss">
	@keyframes linkHover {
		0% {
			font-weight: 400;
		}
		100% {
			font-weight: 500;
		}
	}

	.sticky {
		mask: linear-gradient(var(--red), var(--red), transparent);
		backdrop-filter: blur(0.5rem);
	}

	nav {
		display: flex;
		border-top: 2px solid var(--dark);
		padding-bottom: 1rem;
	}

	.buttons {
		flex-grow: 1;
		display: flex;
		flex-direction: row-reverse;
		gap: 1rem;
	}

	.link {
		font-weight: unset;
		font-variation-settings: 'wght' 400;
		transition: font-variation-settings 0.3s ease-in-out;

		&:hover {
			font-variation-settings: 'wght' 700;
		}
	}
</style>
