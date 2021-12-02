<script lang="ts">
    import CardTitle from "../Atoms/RankCardTitle.svelte";
    import MealCard from "./MealCard.svelte";

    type theme = "white" | "blue";
    type mealDataType = {
        rank: number;
        menu: string;
        vote: number;
    };

    export let theme: theme;
    export let title: string;
    export let mealData: mealDataType[] | null = null;

    // style
    const commonCardStyle: string = "w-5/12 p-7 shadow-2xl rounded-lg";

    const themeList = {
        white: "bg-gray-50",
        blue: "bg-blue-700",
    };
</script>

<div class="{commonCardStyle} {themeList[theme]}">
    <CardTitle title={title} theme={theme} nestedStyle="mb-7" />
    {#each mealData as data, i}
        <MealCard theme={theme} rank={i + 1} menu={data.menu} vote={data.vote} />
    {/each}
</div>