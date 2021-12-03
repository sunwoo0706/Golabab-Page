<script lang="ts">
    type theme = "white" | "blue" | "skeleton";

    export let range: number | null = 0;
    export let theme: theme;

    const rangeWidth: string = range <= 50 ? `${range * 2}%` : "100%";

    // style
    const commonBarStyle: string = `text-right text-xs font-medium h-4 pr-1 rounded-full ${theme === "skeleton" && "hidden"}`;
    const commonWrapBarStyle: string = "flex items-center w-full h-4 rounded-full";

    const barThemeList = {
        white: "text-white bg-blue-600",
        blue: "text-white bg-blue-400",
        skeleton: "hidden"
    };
    
    const wrapBarThemeList = {
        white: "bg-gray-50 border-2 border-blue-600",
        blue: "bg-gray-50",
        skeleton: "bg-gray-300"
    };
</script>

<div class="{commonWrapBarStyle} {wrapBarThemeList[theme]}">
    <div style="width: {rangeWidth}" class="{commonBarStyle} {barThemeList[theme]}">
        {range}
    </div>
</div>

<style lang="scss">
    
</style>
