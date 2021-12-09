<script lang="ts">
    import Logo from '../Atoms/Logo.svelte';
    import NavBar from '../Blocks/NavBar.svelte';
    import NavItem from "../Atoms/NavItem.svelte";

    const href = "https://discord.com/channels/748827810528755772/918315364163653672";
</script>

<header class="flex justify-between items-center w-3/4 py-2.5">
    <Logo />
    <NavBar />
    <nav>
        <NavItem {href} bg="blue">
            Discord
        </NavItem>
    </nav>
</header>

<style lang="scss">
    header {
        margin: 0 auto;
    }
</style>