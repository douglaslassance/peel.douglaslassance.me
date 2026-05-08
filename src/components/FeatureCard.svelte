<script lang="ts">
	import { Card, CardContent } from "$lib/components/ui/card/index.js";

	let { icon: Icon, title, description, delay = "0s", pro = false }: {
		icon: any;
		title: string;
		description: string;
		delay?: string;
		pro?: boolean;
	} = $props();
</script>

<div class="animate-fade-in-up hover:-translate-y-1 transition-all duration-300 relative" style="animation-delay: {delay}">
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
	{#if pro}
		<a
			href="https://douglaslassance.gumroad.com/l/peel-pro"
			target="_blank"
			rel="noopener"
			aria-label="Pro feature — available with Peel Pro"
			class="absolute -top-2 -right-2 inline-flex items-center justify-center px-2.5 py-1 rounded-md text-[10px] font-bold tracking-wider text-white bg-gradient-to-b from-blue-500 to-blue-600 shadow-lg shadow-blue-600/30 ring-1 ring-inset ring-white/20 hover:scale-105 transition-transform duration-200"
		>
			PRO
		</a>
	{/if}
</div>
