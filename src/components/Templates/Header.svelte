<script lang="ts">
    import Logo from '../Atoms/Logo.svelte';
    import NavBar from '../Blocks/NavBar.svelte';
    import NavItem from "../Atoms/NavItem.svelte";
</script>

<header class="flex justify-between items-center w-3/4 py-2.5">
    <Logo />
    <NavBar />
    <nav>
        <NavItem bg="blue">
            Discord
        </NavItem>
    </nav>
</header>

<style lang="scss">
    header {
        margin: 0 auto;
    }
</style>