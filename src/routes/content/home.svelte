<script lang="ts">
	import image from '../../media/home/B.mp4';
	// import image from '../../media/home/D (1).gif';
	// import image from '../../media/home/A (2).png'; //5678-10-13
	// import image from '../../media/home/C (10).png'; //56789-10-12-13
</script>

<div class="h-full w-full">
	<!-- <img src={image} alt="img" class="h-full w-full" /> -->

	<!-- svelte-ignore a11y_media_has_caption -->
	<video src={image} autoplay={true} loop class="h-full w-full object-fill"> </video>
</div>
