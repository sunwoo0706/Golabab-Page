<script lang="ts">
    import RankCard from "../Blocks/RankCard.svelte";
    import Paragraph from "../Blocks/Paragraph.svelte";

    type mealDataType = {
        rank: number;
        menu: string;
        vote: number;
    }

    const dummy: mealDataType[] = [
      {
        rank: 1,
        menu: "아메리카노",
        vote: 8,
      },
      {
        rank: 2,
        menu: "카푸치노",
        vote: 20,
      },
      {
        rank: 3,
        menu: "드립커피",
        vote: 10,
      },
      {
        rank: 4,
        menu: "카페라떼",
        vote: 20,
      },
      {
        rank: 5,
        menu: "케이크",
        vote: 11,
      },
    ];
</script>

<main class="absolute w-3/4 flex justify-around items-center">
    <RankCard theme="blue" title="2주간 급식 순위" mealData={dummy}/>
    <Paragraph />
</main>

<style lang="scss">
    main {
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: fit-content;
    }
</style>