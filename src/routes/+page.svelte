<script lang="ts">
	import type { derived } from 'svelte/store';
	import Button from './components/Button.svelte';
	import Card from './components/Card.svelte';
	import Progressbar from './components/Progressbar.svelte';
	import { data } from './components/data';

	let total: number = data.length;
	let index: number = $state(0);
	let currentQuestion: { question: string; answer: string } = $derived(data[index]);
	let isAnsShown: boolean = $state(false);
	// let flipped: boolean = $derived(isAnsShown);
</script>

<h1>Flash Cards</h1>

<Progressbar {index} {total} />
<div class="container">
	<Card data={currentQuestion} flipped={isAnsShown} />
	<div class="buttons">
		<Button
			name={'< Previous'}
			action={() => {
				if (isAnsShown) {
					isAnsShown = !isAnsShown;        // Hide answer before going back
					setTimeout(() => index--, 250);  // Delay mid-transition    
				} else index--;
			}}
			disable={index === 0}
			style={'nav'}
		/>
		<Button
			name={isAnsShown ? 'Hide Answer' : 'Show Answer'}
			action={() => (isAnsShown = !isAnsShown)}
			disable={null}
			style={'action'}
		/>
		<Button
			name={'Next >'}
			action={() => {
				if (isAnsShown) {
					isAnsShown = !isAnsShown;
					setTimeout(() => index++, 250);
				} else index++;
			}}
			disable={index === total - 1}
			style={'nav'}
		/>
	</div>
</div>

<style>
	* {
		font-family: cursive, sans-serif;
	}
	:root {
		margin: 0 auto;
		padding: 0;
		font-family: cursive, sans-serif;
		max-width: 720px;
        min-width: 320px;
	}

	h1 {
		line-height: 1.5rem;
	}

	.container {
		background-color: #fff;
		border: solid 3px lightgrey;
		border-radius: 10px;
		padding: 0.25rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 0.25rem;
		position: relative;
		perspective: 200vh;
	}

	.buttons {
		width: 100%;
		display: flex;
		justify-content: space-between;
		font-family: cursive, sans-serif;
		border-radius: 5px;
		background-color: #f5f5f5;
	}
</style>
