<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	// Components
	import Navbar from '$lib/components/navbar/Navbar.svelte';
    import Footer from '$lib/components/footer/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<script lang="ts">
		const savedTheme = localStorage.getItem('theme');
		const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

		const theme = savedTheme ?? (prefersDark ? 'dark' : 'light');
		document.documentElement.dataset.theme = theme;
	</script>
</svelte:head>

<div class="bg-amber-100 min-h-screen w-full overflow-x-hidden">
	<div class="grid grid-cols-[1fr] md:grid-cols-[minmax(0,1fr)_minmax(0,4fr)_minmax(0,1fr)] mx-4.5">
		<div aria-hidden="true"></div>
		<div class="min-h-screen grid grid-rows-[auto_1fr_auto]">
			<Navbar/>
			<main class="bg-amber-400">
				{@render children()}
			</main>
			<Footer/>
		</div>
		<div aria-hidden="true"></div>
	</div>
</div>
