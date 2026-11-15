<script>
	import '#lib/styles/app.css';
	import '#lib/styles/defaults.scss';

	import me from '#lib/assets/Me.png';
	import Skills from '#lib/components/skills.svelte';
	import Nav from '#lib/components/nav.svelte';
</script>

<main class="px-4">
	<div class="h-[90vh] flex flex-col">
		<div class="flex-1 flex">
			<h1 class="self-end py-4 title">In solving problems I found out how to make art</h1>
		</div>
	</div>
	<Nav />
	<div class="h-screen flex items-center p-16">
		<div class="flex gap-8 items-center">
			<div class="flex flex-col-reverse">
				<h4>THIS IS ME</h4>
				<img src={me} alt="Me" class="flex-1" />
			</div>
			<div class="">
				<h1>I make things <br /> for people</h1>
				<div class="divider"></div>
				<h2>Communication, Design, Art and Software</h2>
			</div>
		</div>
	</div>
	<div class="h-screen p-16 flex flex-col justify-center">
		<div class="py-8">
			<h1>Using modern <br /> design stacks</h1>
			<h4>What can I say. I’m a gen z developer</h4>
		</div>
		<Skills />
	</div>
</main>

<style lang="scss">
	main {
		background-color: var(--light);
		display: flex;
		flex-direction: column;
		color: var(--dark);
	}
</style>
