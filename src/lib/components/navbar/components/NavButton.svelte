<script lang="ts">
    let {
        children,
        href,
        label
    } = $props<{
        children: () => any,
        href: string,
        label?: string
    }>();
</script>

<a
    class="flex min-w-0 w-full bg-emerald-400"
    href={href}
>
    {@render children()}
    <span class="hidden md:inline min-h-0 min-w-0">
        {label}
    </span>
</a>
