<script lang="ts">
  import { onMount } from "svelte";

    let repoCount = $state<number | undefined>();

    onMount(async () => {
        try {
            const userRes = await fetch("https://api.github.com/users/thenamelessdev/repos?per_page=100");
            if (!userRes.ok) return console.error("Error while getting user repos: ", userRes.status);
            const userJson = await userRes.json() as Object[];

            const orgRes = await fetch("https://api.github.com/orgs/nameless-productions/repos?per_page=100");
            if (!orgRes.ok) return console.error("Error while getting org repos: ", orgRes.status);
            const orgJson = await orgRes.json() as Object[];

            const total = userJson.length + orgJson.length;
            if (isNaN(total)) return console.error("Totas is NaN: ", total);

            repoCount = total;
        } catch (err) {
            console.error("Error while getting repo count ", err)
        }
    })
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