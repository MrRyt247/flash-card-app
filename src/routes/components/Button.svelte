<script lang="ts">
	let { name, action, disable, style } = $props();
</script>

<button onclick={action} disabled={disable} class={style}>
	{name}
</button>

<style>
	button {
		border: none;
		padding: 0.25rem 0.75rem;
		text-align: center;
		font-size: 1.25rem;
		cursor: pointer;
		border-radius: 5px;
		font-family: cursive, sans-serif;
		font-size: clamp(0.75rem, 4vw, 1.35rem);
		background: transparent;
	}

	button:disabled {
		opacity: 0.5;
		cursor: not-allowed;
	}

	.nav {
		color: #4a4a4a;
		font-weight: lighter;
	}

	.action {
		font-weight: bold;
	}
</style>
