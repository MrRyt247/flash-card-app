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
	.container {
		background-color: #fff;
		border: solid 3px lightgrey;
		border-radius: 10px;
		padding: 3px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		position: relative;
	}
</style>
