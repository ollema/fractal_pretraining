<script lang="ts">
	interface Props {
		id?: string | null;
		animate?: boolean;
		restart?: boolean;
		children?: import('svelte').Snippet;
	}

	let { id = null, animate = false, restart = false, children }: Props = $props();
</script>

<section
	data-auto-animate-id={id}
	data-auto-animate={animate || null}
	data-auto-animate-restart={restart || null}
>
	{@render children?.()}
</section>
