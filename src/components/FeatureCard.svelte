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
	<Card class="h-full text-center">
		<CardContent class="flex flex-col items-center pt-8 pb-6 px-6">
			<div class="mb-4 text-primary" aria-hidden="true">
				<Icon size={40} strokeWidth={1.5} />
			</div>
			<h3 class="text-lg font-semibold mb-2">{title}</h3>
			<p class="text-sm text-muted-foreground">{description}</p>
		</CardContent>
	</Card>
</div>
