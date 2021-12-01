<script lang="ts">
    type bgColors = "red" | "blue" | "green" | "yellow" | "gray";

    export let bg: bgColors | null = null;
    export let nestedStyle: string | null = null;
    export let href: string | null = null;

    const bgLogic: string = bg ? `bg-${bg}-600 px-3 py-2 text-white rounded-full` : "hover:underline";
</script>

<a {href} class="font-sans cursor-pointer {bgLogic + " " + nestedStyle}">
    <slot></slot>
</a>