<script lang="ts">
import NavItem from "../Atoms/NavItem.svelte";

    const navItemList: {href: string, text: string}[] = [
        {href: "https://woozy-nut-6be.notion.site/a9897aed1a344b53b0bef9dc55eb54d3", text: "About"},
        {href: "https://golabab.netlify.app/", text: "Promotion"},
        {href: "https://github.com/Team-Dotori", text: "Github"},
    ]
</script>

<nav>
    {#each navItemList as { href, text }}
        <NavItem {href} nestedStyle="mx-2 md:mx-4">
            {text}
        </NavItem>
    {/each}
</nav>