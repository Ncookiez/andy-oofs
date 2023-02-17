<script lang="ts">

	// Imports:
	import OofButton from '$lib/OofButton.svelte';
	
</script>

<!-- #################################################################################################### -->

<!-- SvelteKit Dynamic Header -->
<svelte:head>
	<title>Oof</title>
	<meta name="description" content="Where else can you get free Andy oofs?" />
</svelte:head>

<!-- Page Content -->
<section>
	<OofButton />
</section>

<!-- #################################################################################################### -->

<style>

	section {
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100%;
	}
	
</style>