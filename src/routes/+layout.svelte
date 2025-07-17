<script lang="ts">
	import '../app.css';
	import { Button } from '../lib/components/ui/button';

	let { children } = $props();

	function toggleTheme() {
		document.documentElement.classList.toggle('dark');
	}
</script>

<div class="min-h-screen flex flex-col items-center justify-center">
	{@render children()}
	<Button onclick={toggleTheme} class="mt-4">Toggle Theme</Button>
</div>
