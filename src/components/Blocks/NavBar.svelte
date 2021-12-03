<script lang="ts">
import NavItem from "../Atoms/NavItem.svelte";

    const navItemList: {href: string, text: string}[] = [
        {href: "#", text: "About"},
        {href: "#", text: "Promotion"},
        {href: "#", text: "Github"},
    ]
</script>

<nav>
    {#each navItemList as { href, text }}
        <NavItem {href} nestedStyle="mx-2 md:mx-4">
            {text}
        </NavItem>
    {/each}
</nav>