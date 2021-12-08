<script lang="ts">
  import RankCard from "../Blocks/RankCard.svelte";
  import Paragraph from "../Blocks/Paragraph.svelte";
</script>

<section class="w-3/4 h-screen flex justify-around items-center">
    <RankCard theme="blue" title="2주간 급식 순위" />
    <Paragraph />
</section>

<style lang="scss">
    section {
        margin: 0 auto;
    }
</style>