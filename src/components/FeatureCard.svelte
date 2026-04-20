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
		<CardContent class="flex flex-col pt-6 pb-6 px-6 gap-2">
			<div class="flex items-center gap-2">
				<span class="inline-flex shrink-0 text-foreground/50" aria-hidden="true">
					<Icon size={16} strokeWidth={1.5} />
				</span>
				<h3 class="text-sm font-semibold leading-none">{title}</h3>
			</div>
			<p class="text-sm text-muted-foreground leading-relaxed">{description}</p>
		</CardContent>
	</Card>
</div>
