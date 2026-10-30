<script lang="ts">
    let {tools}: {tools: string[]} = $props()
</script>

<div class="grid lg:grid-cols-5 md:grid-cols-3 sm:grid-cols-1 space-x-1 space-y-2">
    {#each tools as tool}
        <div class="p-1.5 border border-neutral-700 rounded-full w-fit">{tool}</div>
    {/each}
</div>i