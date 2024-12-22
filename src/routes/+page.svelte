<script>
	import SidePanelButton from '../components/side_panel_button.svelte';
	import { tabs } from '../state/tab.svelte';
	import Chords from './content/chords.svelte';
	import FingerPicking from './content/finger_picking.svelte';
	import Home from './content/home.svelte';
	import Music from './content/music.svelte';
	import MusicTheory from './content/music_theory.svelte';
	import OtherResources from './content/other_resources.svelte';
	import Scales from './content/scales.svelte';
	import Strumming from './content/strumming.svelte';
	import Tabs from './content/tabs.svelte';
</script>

<div class="mx-auto flex h-screen w-5/6">
	<!-- Buttons -->
	<div class="my-auto w-1/4">
		<SidePanelButton label={'Home'} />
		<SidePanelButton label={'Music Theory'} />
		<SidePanelButton label={'Chords'} />
		<SidePanelButton label={'Scales'} />
		<SidePanelButton label={'Strumming'} />
		<SidePanelButton label={'Finger Picking'} />
		<SidePanelButton label={'Music'} />
		<SidePanelButton label={'Tabs'} />
		<SidePanelButton label={'Other Resources'} />
	</div>

	<!-- Main -->
	<div class="h-full w-full py-10">
		<div class="h-full w-full overflow-scroll rounded-2xl border border-zinc-600 shadow-2xl">
			<!-- Header -->
			<!-- {#if tabs.selectedTab != 'Home'}
				<div class="bg-black px-8 py-3 text-xl font-bold text-white">
					<h1>{tabs.selectedTab}</h1>
				</div>
			{/if} -->

			<!-- Content -->
			<div class="h-full w-full">
				{#if tabs.selectedTab === 'Home'}
					<Home />
				{:else if tabs.selectedTab === 'Music Theory'}
					<MusicTheory />
				{:else if tabs.selectedTab === 'Chords'}
					<Chords />
				{:else if tabs.selectedTab === 'Scales'}
					<Scales />
				{:else if tabs.selectedTab === 'Strumming'}
					<Strumming />
				{:else if tabs.selectedTab === 'Finger Picking'}
					<FingerPicking />
				{:else if tabs.selectedTab === 'Music'}
					<Music />
				{:else if tabs.selectedTab === 'Tabs'}
					<Tabs />
				{:else if tabs.selectedTab === 'Other Resources'}
					<OtherResources />
				{/if}
			</div>
		</div>
	</div>
</div>
