<script>
	import {  onMount } from "svelte";

	let photos = [];

	onMount(async () => {
		const response = await fetch("https://jsonplaceholder.typicode.com/photos?_limit=10");
		photos = await response.json();
	})
</script>
<style>
	.Photos {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
		grid-gap: 1rem;
	}
</style>

<div class="Photos">
	{#each photos as photo}
	<figure>
		<img src={photo.thumbnailUrl}  alt={photo.title}/>
		<figcaption>{photo.title}</figcaption>
	</figure>
	{:else}
		<p>Cargando</p>
	{/each}
</div>