<script lang="ts">
	let { data, flipped } = $props();

    // let isFlipped: boolean = $derived(flipped);
</script>

<div class="card {flipped ? 'flipped' : ''}">
	<div class="front"><h1>{data.question}</h1></div>
	<div class="back"><p>{data.answer}</p></div>
</div>

<style>
	.card {
		border-radius: 20px;
		position: relative;
		aspect-ratio: 4 / 3;
		width: 100%;
		height: fit-content;
        max-height: 440px;
		transform-style: preserve-3d;
		transition: transform 0.5s ease-in-out;
		padding: 0;
		user-select: none;
		cursor: pointer;
        font-size: clamp(.75rem, 2.4vw, 1.5rem);
	}

	.card.flipped {
		transform: rotateY(180deg);
	}

	.front,
	.back {
		display: flex;
		align-items: center;
		justify-content: center;
		text-align: center;
		position: absolute;
		width: 100%;
		height: 100%;
        max-height: 440px;
		top: 0;
		left: 0;
		backface-visibility: hidden;
		border-radius: 5px;
		background-color: #f5f5f5;
		padding: clamp(1rem, 4vw, 2rem);
		box-sizing: border-box;
	}

	.back {
		transform: rotateY(180deg);
        font-size: clamp(1.25rem, 3.4vw, 1.75rem);
        text-wrap: pretty;
	}
</style>
