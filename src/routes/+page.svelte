<script lang="ts">
	import Progressbar from './components/Progressbar.svelte';
	import { data } from './components/data';

	let total: number = data.length;
	let index: number = $state(0);
</script>

<h1>Flash Cards</h1>

<Progressbar {index} {total} />