<script lang="ts">
	import '../app.css';
	import Header from '../lib/components/layout/Header.svelte';

	let { children } = $props();
</script>

<div class="min-h-screen flex flex-col">
	<Header />
	<main class="flex-grow flex flex-col items-center justify-center">
		{@render children()}
	</main>
</div>
