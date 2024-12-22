<script lang="ts">
	import image from '../../media/home/G (12).png';
	import ContentLayout from '../../components/content_layout.svelte';
	import { content } from '../../state/content.svelte';

	let showContent = $state(false);
</script>

<div class="h-full w-full">
	{#if showContent == false}
		<!-- svelte-ignore a11y_click_events_have_key_events -->
		<!-- svelte-ignore a11y_no_static_element_interactions -->
		<div class="relative h-full w-full" onclick={() => (showContent = !showContent)}>
			<img src={image} alt="" class="h-full w-full" />
		</div>
	{/if}

	{#if showContent}
		<ContentLayout
			books={content.content.musicTheory.books}
			links={content.content.musicTheory.links}
			youtubes={content.content.musicTheory.youtube}
			customVideos={content.content.musicTheory.customVideo}
		/>
	{/if}
</div>
