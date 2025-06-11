<script lang="ts">
	interface Props {
		name?: string;
		external?: boolean;
		children?: import('svelte').Snippet;
	}

	let { name = 'example.md', external = false, children }: Props = $props();
</script>

{#if external}
	<section data-markdown={name}></section>
{:else}
	<section data-markdown>
		<div data-template>
			{@render children?.()}
		</div>
	</section>
{/if}
