<script lang="ts">

	// Imports:
	import Footer from '$lib/Footer.svelte';
	import '../app.css';
	
</script>

<!-- #################################################################################################### -->

<!-- App Content -->
<main><slot /></main>

<!-- Footer -->
<Footer />

<!-- #################################################################################################### -->

<style>

	main {
		height: 100vh;
		width: 100vw;
		padding: 1em;
	}

</style>