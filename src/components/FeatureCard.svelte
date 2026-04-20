<script lang="ts">
	import { Card, CardContent } from "$lib/components/ui/card/index.js";

	let { icon: Icon, title, description, delay = "0s" }: {
		icon: any;
		title: string;
		description: string;
		delay?: string;
	} = $props();
</script>

<div class="animate-fade-in-up hover:-translate-y-1 transition-all duration-300" style="animation-delay: {delay}">
	<Card class="h-full">
		<CardContent class="flex flex-col px-5 gap-3">
			<div class="flex items-center gap-2">
				<span class="inline-flex size-4 shrink-0 items-center justify-center text-foreground/50" aria-hidden="true">
					<Icon size={16} strokeWidth={1.5} />
				</span>
				<h3 class="text-sm font-semibold leading-none">{title}</h3>
			</div>
			<p class="text-sm text-muted-foreground leading-relaxed">{description}</p>
		</CardContent>
	</Card>
</div>
