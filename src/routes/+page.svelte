<script>
	import '#lib/styles/app.css';
	import '#lib/styles/defaults.scss';

	import Skills from '#lib/components/skills.svelte';
	import Nav from '#lib/components/nav.svelte';
	import AboutMe from '#lib/components/aboutMe.svelte';
	import BlogPosts from '#lib/components/blogPosts.svelte';

	// fetch('https://raw.githubusercontent.com/ellk-itu/portfolio/master/blog/').then((file) =>
	// 	file.text()
	// );
</script>

<main class="px-4">
	<div class="h-[90vh] flex flex-col">
		<div class="flex-1 flex">
			<h1 class="self-end py-4 title">In solving problems I found out how to make art</h1>
		</div>
	</div>
	<Nav />
	<AboutMe />
	<Skills />
	<BlogPosts />
</main>

<style lang="scss">
	main {
		background-color: var(--light);
		display: flex;
		flex-direction: column;
		color: var(--dark);
	}
</style>
