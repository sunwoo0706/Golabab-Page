<script lang="ts">
    import ErrorCard from "../Atoms/ErrorCard.svelte";
    import LoadingCard from "../Atoms/LoadingCard.svelte";
    import CardTitle from "../Atoms/RankCardTitle.svelte";
    import MealCard from "./MealCard.svelte";

    type theme = "white" | "blue";

    type mealDataListType = {
        menuName: string;
        numOfVote: number;
    }

    type mealDataType = {
        list: mealDataListType[];
    }
  
    const uri: string = "http://10.120.73.152:8080/api/v1/views/menu-ranking?start=0&end=7&range=total";

    const sleep = (ms: number) => {
        return new Promise((r) => setTimeout(r, ms));
    };

    const getMealData = async () => {
        const res = await fetch(uri);
		const data: mealDataType = await res.json();
        const mealData: mealDataListType[] = data.list;

        await sleep(250);

        if (res.ok) {
			return mealData;
		} else {
			throw new Error(`${res.status}`);
		}
    };

    export let theme: theme;
    export let title: string;

    // style
    const commonCardStyle: string = "w-full xl:w-5/12 p-7 shadow-2xl rounded-lg";

    const themeList = {
        white: "bg-gray-50",
        blue: "bg-blue-700",
    };
</script>

<div class="{commonCardStyle} {themeList[theme]}">
    <CardTitle title={title} theme={theme} nestedStyle="mb-7" />
    {#await getMealData()}
        <LoadingCard />
    {:then mealDataList}
    {#each mealDataList as { menuName, numOfVote }, i}
        <MealCard theme={theme} rank={i + 1} menu={menuName} vote={numOfVote} />
    {/each}
    {:catch err}
        <ErrorCard />
    {/await}
</div>