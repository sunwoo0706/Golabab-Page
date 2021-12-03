<p class="font-sans text-3xl leading-relaxed italic font-semibold hidden xl:block">
    <span id="fade-1" class="inline-block"><span class="text-7xl font-bold">골라밥</span>&nbsp;은 더 나은 급식 경험을</span><br />
    <span id="fade-2" class="inline-block">학생분들에게 제공하기 위해</span><br />
    <span id="fade-3" class="inline-block">끊임없이 노력하겠습니다.</span>
</p>

<style lang="scss">
    $i: 1;

    @keyframes fadeInLeft {
        0% {
            opacity: 0;
            transform: translateX(-20px);
        }
        100% {
            opacity: 1;
            transform: translateX(0);
        }
    }
    @while $i <= 3 {
        #fade-#{$i} {
            animation: fadeInLeft 1s #{$i}s both;
        }
        $i: $i + 1;
    }
</style>