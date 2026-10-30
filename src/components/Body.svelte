<script>
  import GithubStats from "./GithubStats.svelte";
import ToolList from "./ToolList.svelte";

</script>
<div class="mt-15">
    <p class="text-green-400">Hi, I'm</p>
    <p class="text-4xl font-bold">Nameless</p>
    <br>
    <p class="text-gray-500">Self-taught developer building web apps, Discord bots and a homelab.</p>
    <br>
    <a href="https://github.com/thenamelessdev" class="button" target="_blank">Github</a>

    <br><br>

    <GithubStats />

    <br><br>

    <p class="text-2xl">What I work with</p>
    <ToolList tools={["TypeScript", "JavaScript", "Go", "Svelte", "SvelteKit", "DiscordGo", "Discord.js", "React", "Next.js", "Prisma"]}/>
</div>