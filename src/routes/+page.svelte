<script lang="ts">
	import Card from './components/Card.svelte';
	import Progressbar from './components/Progressbar.svelte';
	import { data } from './components/data';

	let total: number = data.length;
	let index: number = $state(0);
	let currentQuestion: { question: string; answer: string } = data[index];
	let isAnsShown: boolean = $state(false);
</script>

<h1>Flash Cards</h1>

<Progressbar {index} {total} />
<div class="container">
	<Card data={currentQuestion} />
</div>

<style>
    h1 {
        line-height: 1rem;
    }
	.container {
		background-color: #fff;
		border: solid 3px lightgrey;
		border-radius: 10px;
		padding: 3px;
		display: flex;
        flex-direction: column;
		align-items: center;
		justify-content: center;
        aspect-ratio: 4/3;
		position: relative;
        perspective: 100vh;
	}

    :root {
        margin: 0 auto;
        padding: 0;
        font-family: cursive, sans-serif;
        max-width: 720px;
    }
</style>
