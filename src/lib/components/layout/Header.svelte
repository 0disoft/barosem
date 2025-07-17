<script lang="ts">
	import { Button } from '../ui/button';
	import Sun from 'lucide-svelte/icons/sun';
	import Moon from 'lucide-svelte/icons/moon';

	function toggleTheme() {
		document.documentElement.classList.toggle('dark');
	}

	let currentTheme = $state('');

	$effect(() => {
		currentTheme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
	});
</script>

<header class="w-full p-4 border-b border-border flex justify-center items-center">
	<div class="container flex justify-between items-center">
		<a href="/" class="text-2xl font-bold">BaroSem</a>
		<Button onclick={toggleTheme} variant="ghost" size="icon" class="relative">
			<Sun class="h-[1.2rem] w-[1.2rem] text-foreground transition-all duration-300 {currentTheme === 'light' ? 'opacity-100 rotate-0' : 'opacity-0 -rotate-90'}" />
			<Moon class="h-[1.2rem] w-[1.2rem] text-foreground absolute transition-all duration-300 {currentTheme === 'dark' ? 'opacity-100 rotate-0' : 'opacity-0 rotate-90'}" />
			<span class="sr-only">Toggle theme</span>
		</Button>
	</div>
</header>