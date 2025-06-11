<script lang="ts">
	interface Props {
		id?: string | null;
		lines?: string | boolean | null;
		noescape?: boolean;
		children?: import('svelte').Snippet;
	}

	let { id = null, lines = null, noescape = false, children }: Props = $props();
</script>

<pre data-id={id || null}>
  <code data-trim data-line-numbers={lines || null} data-noescape={noescape || null}>
    {@render children?.()}
  </code>
</pre>
