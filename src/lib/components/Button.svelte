<script lang="ts">
    let { 
        children, 
        class: className = '', 
        onClick
    } = $props<{
        children: () => any,
        class?: string,
        onClick?: () => void
    }>();
</script>

<button
    class={className}
    onclick={onClick}
>
    {@render children()}
</button>
