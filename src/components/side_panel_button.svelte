<script lang="ts">
	import { tabs } from '../state/tab.svelte';

	let { label }: { label: string } = $props();
</script>

<div class="flex items-center justify-center py-2">
	<!-- svelte-ignore a11y_click_events_have_key_events -->
	<!-- svelte-ignore a11y_no_static_element_interactions -->
	<div
		class={tabs.selectedTab.toString().toLowerCase() == label.toString().toLowerCase()
			? 'w-full cursor-pointer rounded-full border border-black bg-black py-2 text-center text-white shadow-2xl'
			: 'w-full cursor-pointer rounded-full border border-zinc-300 py-2 text-center hover:border-black hover:shadow-xl'}
		onclick={() => (tabs.selectedTab = label)}
	>
		<span class="font-semibold">
			{label}
		</span>
	</div>
	<div
		class={tabs.selectedTab.toString().toLowerCase() == label.toString().toLowerCase()
			? 'h-[1px] w-10 border-t border-zinc-600'
			: 'h-[1px] w-10'}
	></div>
</div>
