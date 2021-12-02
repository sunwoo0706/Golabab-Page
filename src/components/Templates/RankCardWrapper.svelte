<script lang="ts">
  import RankCard from "../Blocks/RankCard.svelte";
  import Paragraph from "../Blocks/Paragraph.svelte";
</script>

<main class="absolute w-3/4 flex justify-around items-center">
    <RankCard theme="blue" title="2주간 급식 순위" />
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