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
		aspect-ratio: 1 / 1;
		width: 100%;
		height: 100%;
		transform-style: preserve-3d;
		transition: transform 0.4s ease-in-out;
		padding: 0;
		user-select: none;
		cursor: pointer;
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
		height: inherit;
		top: 0;
		left: 0;
		backface-visibility: hidden;
		border-radius: 5px;
		background-color: #f5f5f5;
		padding: 1rem;
		box-sizing: border-box;
	}

	.back {
		transform: rotateY(180deg);
		font-size: 1.75rem;
	}
</style>
