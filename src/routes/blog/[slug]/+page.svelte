<script lang="ts">
	import { marked } from 'marked';
	import type { PageProps } from './$types';
	import SvelteMarkdown from 'svelte-markdown';
	import '#lib/styles/defaults.scss';
	import '#lib/styles/app.css';

	let { params }: PageProps = $props();

	const getPage = async () => {
		const res = await fetch(
			`https://cdn.jsdelivr.net/gh/ellk-itu/portfolio@master/blog/${params.slug}.md`
		);

		return await res.text();
	};

	let page = $state('');

	$effect(() => {
		getPage().then((text) => (page = text));
	});

	let tokens = $derived(marked.lexer(page));
</script>

<SvelteMarkdown source={tokens} />
