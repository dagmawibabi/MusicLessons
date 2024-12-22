<script lang="ts">
	let { video } = $props();

	import Youtube from 'svelte-youtube-embed';
</script>

<div class="p-4">
	<div
		class="group cursor-pointer overflow-clip rounded-xl border border-zinc-300 shadow-md transition-all hover:scale-105 hover:border-black hover:shadow-2xl"
	>
		<div>
			<Youtube id="EBtsu6naB8g" thumbnail="" play_button="" />
			<div class="grid py-1 pl-3">
				<span class="font-semibold">
					{video.title}
				</span>
				<span class="text-sm">
					by {video.author}
				</span>
			</div>
		</div>
		<!-- <div class="border-b border-black px-3 py-2">
			<span class=""> Hallelujah by Alexandra Burke</span>
		</div> -->
		<!-- svelte-ignore a11y_media_has_caption -->
		<!-- <video src={Hallelujah}> </video> -->

		<!-- <div class="relative">
			<div
				class="absolute flex h-full w-full items-center justify-center bg-white bg-opacity-30 backdrop-blur-sm transition-all hover:bg-opacity-0 hover:opacity-0 hover:backdrop-blur-none"
			>
				<div class="rounded-full border border-white bg-white px-4 py-1 group-hover:border-black">
					<span> {data.title} by {data.artist}</span>
				</div>
			</div>
			svelte-ignore a11y_media_has_caption
			<video src={data['link']} muted autoplay loop> </video>
		</div> -->
	</div>
</div>
