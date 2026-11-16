<script lang="ts">
	interface Path {
		files: Path[];
		name: string;
		type: 'directory' | 'file';
	}

	let blogFiles: Path | null = $state(null);

	const fetchBlogPosts = async () => {
		const res = await fetch(`https://data.jsdelivr.com/v1/packages/gh/ellk-itu/portfolio@master`);
		const json = await res.json();
		const blogpost = json.files.find((e: Path) => e.type === 'directory' && e.name === 'blog');
		blogFiles = blogpost;
	};

	$effect(() => {
		if (!blogFiles) {
			fetchBlogPosts();
		}
	});
</script>

<div class="blog-posts">
	{#if blogFiles}
		{#each blogFiles.files as blogFile (blogFile.name)}
			<div class="item">
				<h5>{blogFile.name.split('.')[0]}</h5>
			</div>
		{/each}
	{/if}
</div>
