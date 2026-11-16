<script lang="ts">
	import { goto } from '$app/navigation';

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
	<h1>This is what I've made</h1>
	<div class="flex flex-wrap">
		{#if blogFiles}
			{#each blogFiles.files as blogFile (blogFile.name)}
				<div class="item" onclick={() => goto(`/blog/${blogFile.name.split('.')[0]}`)}>
					<h5>{blogFile.name.split('.')[0]}</h5>
					<img
						src={`https://cdn.jsdelivr.net/gh/ellk-itu/portfolio@master/blog/images/${blogFile.name.split('.')[0]}.jpeg`}
						alt=""
					/>
				</div>
			{/each}
		{/if}
	</div>
</div>

<style lang="scss">
	.item {
		position: relative;
		flex-grow: 1;
		align-items: center;
		justify-items: center;

		h5 {
			position: relative;
			z-index: 10;
			pointer-events: none;
		}

		img {
			filter: grayscale(100%) blur(0.1rem);
			transition: ease-in-out 0.2s;
			object-fit: cover;
			position: absolute;
			top: 0;

			&:hover {
				filter: grayscale(0%) blur(0px);
			}
		}
	}
</style>
