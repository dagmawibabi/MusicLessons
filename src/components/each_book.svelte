<script lang="ts">
	let { book } = $props();
	import { BookText } from 'lucide-svelte';
</script>

<div class="p-1">
	<div
		class="flex w-[90%] cursor-pointer items-center gap-x-3 rounded-xl border border-zinc-300 px-4 shadow-md transition-all hover:scale-105 hover:border-black hover:shadow-2xl"
	>
		<BookText size={30} />
		<div class="flex flex-col py-2">
			<span class="font-semibold">
				{book.title}
			</span>
			<span class="text-sm">
				By {book.author}
			</span>
		</div>
	</div>
</div>
