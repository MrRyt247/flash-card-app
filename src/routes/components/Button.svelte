<script lang="ts">
	let { name, action, disable, style } = $props();
</script>

<button onclick={action} disabled={disable} class={style}>
	{name}
</button>

<style>
	button {
		border: none;
		padding: .25rem .75rem;
		text-align: center;
		font-size: 1.25rem;
		/* margin: 4px 2px; */
		cursor: pointer;
		border-radius: 5px;
        font-family: cursive, sans-serif;
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
