<script lang="ts">
	import { onMount } from 'svelte';

	import Reveal from 'reveal.js';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Notes from 'reveal.js/plugin/notes/notes';
	import KaTeX from 'reveal.js/plugin/math/math';

	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/white.css';
	import 'reveal.js/plugin/highlight/monokai.css';

	import Presentation from './presentation.svelte';

	onMount(() => {
		const deck = new Reveal({
			plugins: [Markdown, Highlight, Notes, KaTeX],
			autoAnimate: false,
			transition: 'none',
			hash: true,
			center: false
		});

		deck.initialize({
			width: 1512,
			height: 982
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<Presentation />
	</div>
</div>
