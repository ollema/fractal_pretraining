<script lang="ts">
	import DeltaPicker from './delta-picker.svelte';
	import Markdown from './markdown.svelte';
	import SigmaPicker from './sigma-picker.svelte';
	import Slide from './slide.svelte';
</script>

<Slide>
	<div class="title-slide">
		<h2>Scaling Backwards: Minimal Synthetic Pre-training?</h2>
		<h3>Ryo Nakamura et al.</h3>
		<h3>Zenseact Deep Learning Study Circle</h3>
		<h4>2025-06-13 - Olle Månsson</h4>
		<img src="1p-frac.png" alt="1p-frac" />
	</div>
</Slide>
<Markdown name="01-introduction.md" external />
<Markdown name="02-background.md" external />
<Markdown name="03-method.md" external />
<Markdown name="04-experiments.md" external />
<Slide>
	<DeltaPicker />
</Slide>
<Markdown name="05-experiments.md" external />
<Slide>
	<SigmaPicker />
</Slide>
<Markdown name="06-experiments.md" external />
<Markdown name="07-conclusion.md" external />

<!-- <Markdown name="99-applications.md" external /> -->

<style>
	.title-slide {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		height: 100%;
	}

	img {
		margin-top: 1em;
	}
</style>
