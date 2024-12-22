<script lang="ts">
	import EachBook from './each_book.svelte';
	import EachLink from './each_link.svelte';
	import EachVideo from './each_video.svelte';
	import EachYoutubeVideo from './each_youtube_video.svelte';

	let { books, links, youtubes, customVideos } = $props();
</script>

<div class="h-full w-full">
	<!-- Books -->
	{#if books.length > 0}
		<div>
			<div class="bg-zinc-950 py-2 text-center font-mono text-xl font-bold text-white">Books</div>
			<div class="grid grid-cols-3 gap-y-4 px-4 pb-10 pt-5">
				{#each books as book}
					<EachBook {book} />
				{/each}
			</div>
		</div>
	{/if}

	<!-- Links -->
	{#if links.length > 0}
		<div>
			<div class="bg-zinc-950 py-2 text-center font-mono text-xl font-bold text-white">Links</div>
			<div class="grid grid-cols-3 gap-y-4 px-4 pb-10 pt-5">
				{#each links as link}
					<EachLink {link} />
				{/each}
			</div>
		</div>
	{/if}

	<!-- YouTube Videos -->
	{#if youtubes.length > 0}
		<div>
			<div class="bg-zinc-950 py-2 text-center font-mono text-xl font-bold text-white">Videos</div>
			<div class="grid grid-cols-3 px-4 pb-10 pt-5">
				{#each youtubes as video}
					<EachYoutubeVideo {video} />
				{/each}
			</div>
		</div>
	{/if}

	<!-- Custom Videos -->
	{#if customVideos.length > 0}
		<div>
			<div class="bg-zinc-950 py-2 text-center font-mono text-xl font-bold text-white">
				Custom Videos
			</div>
			<div class="grid grid-cols-2 px-4 pb-10 pt-5">
				{#each customVideos as customVideo}
					<EachVideo {customVideo} />
				{/each}
			</div>
		</div>
	{/if}
</div>
