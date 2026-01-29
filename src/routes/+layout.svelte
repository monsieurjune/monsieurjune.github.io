<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<script lang="ts">
		const saved = localStorage.getItem('theme');
		const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

		const theme = saved ?? (prefersDark ? 'dark' : 'light');
		document.documentElement.dataset.theme = theme;
	</script>
</svelte:head>

<div class="min-h-screen grid grid-rows-[auto_1fr_auto]">
	<header>
	</header>
	<main class="bg-bg">
		{@render children()}
	</main>
	<footer>
	</footer>
</div>
