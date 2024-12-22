<script lang="ts">
	let { link } = $props();
	import { Link2 } from 'lucide-svelte';
</script>

<div class="p-1">
	<div
		class="flex w-[90%] cursor-pointer items-center gap-x-3 rounded-xl border border-zinc-300 px-4 shadow-md transition-all hover:scale-105 hover:border-black hover:shadow-2xl"
	>
		<Link2 size={30} />
		<div class="flex flex-col py-2">
			<span class="font-semibold">
				{link.title}
			</span>
			<span class="text-sm">
				{link.source}
			</span>
		</div>
	</div>
</div>
