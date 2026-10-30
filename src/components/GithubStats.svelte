<script lang="ts">
    let repoCount = $state<number | undefined>();
</script>

<div class="flex border border-neutral-700 p-2 rounded-xl">
    <div>
        <a href="https://github.com/thenamelessdev" class="text-sm text-gray-400">github.com/thenamelessdev</a>
        <br>
        <p class="text-2xl">GitHub stats</p>
    </div>

    <div class="ml-auto">
        <p class="text-xl text-green-200">{repoCount ?? "Loading..."}</p>
        
        <p class="font-bold">Repo count</p>
    </div>
</div>