<script lang="ts">
    type theme = "blue" | "white";

    export let title: string;
    export let theme: theme;
    export let nestedStyle: string | null = null;

    // style
    const commonCardStyle = "w-full p-3 pl-4 shadow-inner font-sans font-bold text-2xl rounded-lg";

    // 부모의 테마와 반대되는 컬러로 자식의 컬러를 지정한다.
    const themeList = {
        white: "text-gray-50 bg-blue-700",
        blue: "text-blue-600 bg-gray-50",
    };
</script>

<h3 class="{commonCardStyle} {themeList[theme]} {nestedStyle}">
    {title}
</h3>