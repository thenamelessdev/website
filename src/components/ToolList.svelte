<script lang="ts">
    let {tools}: {tools: string[]} = $props()
</script>

<div class="flex flex-wrap gap-2">
    {#each tools as tool}
        <div class="p-1.5 border border-neutral-700 rounded-full w-fit">{tool}</div>
    {/each}
</div>