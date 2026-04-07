<script lang="ts">
    let {
        value,
        onThemeChange
    } = $props<{
        value?: string
        onThemeChange?: (val: string) => void
    }>();

    function setTheme(val: string) {
        value = val;
        onThemeChange?.(val);
    }
</script>

<div class="relative bg-amber-400 inline-flex rounded-full gap-x-2 px-2 py-0.5">
    <div
		class="absolute inset-0 w-1/2 rounded-full bg-gray-600 opacity-30 transition-transform duration-200"
		style="transform: translateX({value === 'light' ? '0%' : '100%'})"
	>
    </div>
    <button
        class="relative z-10 grid place-items-center rounded-full px-2 py-0.5"
        onclick={() => setTheme('light')}
    >
        L
    </button>
    <button
        class="relative z-10 grid place-items-center rounded-full px-2 py-0.5"
        onclick={() => setTheme('dark')}
    >
        D
    </button>
</div>
