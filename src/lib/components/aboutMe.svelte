<script lang="ts">
	import me from '#lib/assets/Me.png';
</script>

<div class="min-h-screen flex items-center about-me">
	<div class="flex gap-8 items-center flex-wrap-reverse justify-center-safe">
		<div class="flex flex-col-reverse image-container">
			<h4>THIS IS ME</h4>
			<img src={me} alt="Me" class="flex-1" />
		</div>
		<div class="flex-1">
			<h1>I make things <br /> for people</h1>
			<div class="divider"></div>
			<h2>Communication, Design, Art and Software</h2>
		</div>
	</div>
</div>

<style lang="scss">
	.about-me {
		padding: max(0px, calc(var(--font-size) * 4 - 2rem));
		& .image-container {
			width: min(90vw, 450px);
		}
	}
</style>
