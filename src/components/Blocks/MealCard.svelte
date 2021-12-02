<script lang="ts">
    import RankBar from '../Atoms/RankBar.svelte';

    type theme = "white" | "blue";

    export let rank: number;
    export let menu: string;
    export let vote: number;
    export let theme: theme;
</script>

<article class="w-full py-3.5">
    <div class="pl-1 mb-1 font-sans font-bold text-sm text-white {theme === "white" && "text-blue-600"}">
        {rank}위 {menu}
    </div>
    <RankBar theme={theme} range={vote}/>
</article>