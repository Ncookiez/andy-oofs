<script lang="ts">

	// Initializations:
	const githubUser = 'Ncookiez';
	const githubLink = `https://github.com/${githubUser}`;
	
</script>

<!-- #################################################################################################### -->

<footer>

	<!-- Footer Content -->
	<span>Made with </span>
	<i id="heart" />
	<span> by <a href="{githubLink}">Ncookie</a></span>

</footer>

<!-- #################################################################################################### -->

<style>

	footer {
		position: fixed;
		bottom: 0;
		justify-content: center;
		align-items: center;
		display: flex;
		height: 48px;
		width: 100%;
		color: rgba(255, 255, 255, 0.65);
		background: transparent;
		font-size: 60%;
		font-weight: 800;
		letter-spacing: 0.5px;
		text-transform: uppercase;
	}
	
	footer span a {
		color: inherit;
		transition: color;
	}
	
	footer a:hover {
		color: rgba(255, 255, 255, 1);
	}
	
	#heart {
		width: 40px;
		height: 40px;
		margin: 0 -8px;
		background: transparent url('/images/heart.png') no-repeat;
		background-size: 2900%;
	}
	
	#heart:hover {
		background-position: right;
		animation: moveHeart 800ms steps(28) forwards;
	}
	
	@keyframes moveHeart {
		0% { background-position: left; }
		50% { background-position: right; }
		100% { background-position: right; }
	}
	
</style>