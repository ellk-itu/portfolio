<script lang="ts">
	import '#lib/styles/defaults.scss';
	import '#lib/styles/app.css';
	import { marked } from 'marked';
	import type { PageProps } from './$types';
	import SvelteMarkdown from 'svelte-markdown';

	let { params }: PageProps = $props();

	const getPage = async () => {
		const res = await fetch(
			`https://raw.githubusercontent.com/ellk-itu/portfolio/master/blog/${params.slug}.md`
		);

		return await res.text();
	};

	let page = $state('');

	$effect(() => {
		getPage().then((text) => (page = text));
	});

	let tokens = $derived(marked.lexer(page));
</script>

<h1>{params.slug}</h1>
<SvelteMarkdown source={tokens} />
