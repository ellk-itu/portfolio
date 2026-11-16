<script lang="ts">
	import favicon from '#lib/assets/favicon.svg';
	import { browser } from '$app/env';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();

	if (browser) {
		const preferDarkMode = window.matchMedia('(prefers-color-scheme: dark)');

		if (preferDarkMode && preferDarkMode.matches) document.body.setAttribute('data-theme', 'dark');
	}
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
