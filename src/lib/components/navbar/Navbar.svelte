<script lang="ts">
    import NavButton from "./components/NavButton.svelte";
    import ThemeSwitcher from "./components/ThemeSwitcher.svelte";

    let {
        onThemeChange,
    } = $props<{
        onThemeChange?: (val: string) => void
    }>();
</script>

<nav class="bg-gray-300 grid grid-cols-[auto_1fr] md:grid-cols-2 min-w-0 w-full justify-between px-3 py-1.5">
    <a href="/">
        <span>
            O
        </span>
        <span>
            Name
        </span>
    </a>
    <div>
        d
    </div>
    <ThemeSwitcher/>
</nav>

<!-- <header class="fixed inset-x-0 top-4 z-50 flex justify-center">
    <nav class="w-[calc(100%-2rem)] max-w-7xl rounded-xl bg-white shadow-xl grid grid-cols-[auto_1fr] md:grid-cols-2 min-w-0 justify-between px-3 py-1.5">
        <header class="min-w-0">
            Name
        </header>
        <div class="flex min-w-0 w-full justify-between">
            <div class="flex min-w-0 w-full gap-6">
                <NavButton href="/">Home</NavButton>
                <NavButton href="/projects">Projects</NavButton>
                <NavButton href="/contributions">Contributions</NavButton>
                <NavButton href="/blogs">Blogs</NavButton>
                <NavButton href="/resume">Resume</NavButton>
            </div>
            <ThemeSwitcher />
        </div>
    </nav>
</header> -->