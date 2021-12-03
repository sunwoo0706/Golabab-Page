<script>
import SkeletonCard from "../Atoms/SkeletonCard.svelte";

</script>
{#each [...Array(7)] as i}
    <SkeletonCard theme="skeleton"/>
{/each}