<script lang="ts">
	let { customVideo } = $props();
</script>

<div class="p-4">
	<div
		class="group cursor-pointer overflow-clip rounded-xl border border-zinc-300 shadow-md transition-all hover:scale-105 hover:border-black hover:shadow-2xl"
	>
		<!-- <div class="border-b border-black px-3 py-2">
			<span class=""> Hallelujah by Alexandra Burke</span>
		</div> -->
		<!-- svelte-ignore a11y_media_has_caption -->
		<!-- <video src={Hallelujah}> </video> -->

		<div class="relative">
			<div
				class="absolute flex h-full w-full items-center justify-center bg-white bg-opacity-30 backdrop-blur-sm transition-all hover:bg-opacity-0 hover:opacity-0 hover:backdrop-blur-none"
			>
				<div class="rounded-full border border-white bg-white px-4 py-1 group-hover:border-black">
					<span> {customVideo.title} by {customVideo.artist}</span>
				</div>
			</div>
			<!-- svelte-ignore a11y_media_has_caption -->
			<video src={customVideo['link']} muted autoplay loop> </video>
		</div>
	</div>
</div>
