<script lang="ts">
	let { total, index } = $props();

    let currentQuestion = index + 1;
	let progress: number = (currentQuestion / total) * 100;
</script>

<div class="container" style:--progress={progress}%>
	<div class="bar"></div>
	<span>{currentQuestion} of {total}</span>
</div>

<style>
	.container {
		background-color: #fff;
		border: solid 3px lightgrey;
		border-radius: 10px;
		padding: 3px;
		display: flex;
		align-items: center;
		justify-content: space-between;
        margin-bottom: 1rem;
        position: relative;
	}

	.bar {
		width: var(--progress);
		height: 2rem;
		background-color: lightgrey;
		border-radius: 5px;
	}

	span {
        position: absolute;
        top: 50%;
        right: 0;
		transform: translate(-25%, -50%);
		font-size: 1rem;
		color: #333;
	}
</style>
