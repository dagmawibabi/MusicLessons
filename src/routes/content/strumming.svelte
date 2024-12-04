<script lang="ts">
	import EachVideo from '../../components/each_video.svelte';
	import image from '../../media/home/C (12).png';
	let showContent = $state(false);
</script>

<div class="h-full w-full">
	{#if showContent == false}
		<!-- svelte-ignore a11y_click_events_have_key_events -->
		<!-- svelte-ignore a11y_no_static_element_interactions -->
		<div class="relative h-full w-full" onclick={() => (showContent = !showContent)}>
			<!-- <div class="absolute flex h-full w-full items-center justify-center self-center border">
			<div class="rounded-full border-2 border-blue-600 bg-black px-16 py-1 text-white">GO</div>
		</div> -->
			<img src={image} alt="" class="h-full w-full" />
		</div>
	{/if}

	{#if showContent}
		<div class="h-full w-full">
			<div class="grid grid-cols-2 px-3 py-2">
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
				<EachVideo />
			</div>
		</div>
	{/if}
</div>
