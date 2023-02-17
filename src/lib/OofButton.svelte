<script lang="ts">

	// Imports:
	import { onMount } from 'svelte';

	// Initializations:
	const oofs: Record<number, HTMLAudioElement> = {};
	let buttonClicked: boolean = false;

	const playRandomOof = () => {
		const oofId = Math.floor(Math.random() * Object.keys(oofs).length);
		const oofAudio = oofs[oofId];
		oofAudio.currentTime = 0;
		oofAudio.play();
		if(!buttonClicked) { buttonClicked = true };
	}

	onMount(() => {
		oofs[0] = new Audio('/oofs/andy-oof-1.mp3');
		oofs[1] = new Audio('/oofs/andy-oof-2.mp3');
		oofs[2] = new Audio('/oofs/andy-oof-3.mp3');
	});

</script>

<!-- #################################################################################################### -->

<div class="buttonWrapper">
	<div class="oofButton" on:click={playRandomOof} on:keydown={playRandomOof}>
		<img src="/images/andy-pfp.webp" alt="Andy PFP">
	</div>
	{#if !buttonClicked}
		<span class="helper">^ Click Andy ^</span>
	{/if}
</div>

<!-- #################################################################################################### -->

<style>

	.buttonWrapper {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.oofButton {
		cursor: pointer;
		user-select: none;
	}

	.oofButton > img {
		height: 20vh;
		width: auto;
		border-radius: 50%;
		transition: all .1s;
		aspect-ratio: 1/1;
	}

	.oofButton:hover > img {
		height: 21vh;
	}

	.helper {
		position: absolute;
		top: calc(100% + 1em);
	}
	
</style>
