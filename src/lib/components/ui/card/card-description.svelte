<script lang="ts">
	import type { HTMLAttributes } from "svelte/elements";
	import { cn } from "$lib/shadcn.js";

	type $$Props = HTMLAttributes<HTMLParagraphElement>;

	interface Props {
		class?: $$Props["class"];
		children?: import('svelte').Snippet;
		[key: string]: any
	}

	let { class: className = undefined, children, ...rest }: Props = $props();
	
</script>

<p class={cn("text-muted-foreground text-sm", className)} {...rest}>
	{@render children?.()}
</p>
