<script>
    import CtAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    import Speaker from "./Speaker.svelte";
</script>
<SectionWrapper>
    <div class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14">
        <h2 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold">
            <span class="text-indigo-400">Tech</span> is <span class="text-slate-600 line-through">Temporary</span> <span class="text-green-400">Timeless</span>
        </h2>
        <p class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">Join the world's top tech minds for an immersive experience in <span class="italic">AI, Web3, and Future Innovations!</span> and much more.</p>
        <CtAs />
        <div class="flex item-center justify-center gap-2 text-base">
            <p>4.6</p>
            {#each [0,1,2,3,4] as ind}
                <div class="grid place-items-center relative">
                    <i class="fa-solid fa-star opacity-0"></i>
                    <div class={"absolute left-0 grid place-items-center " + (ind===4 ? "w-[60%] overflow-hidden": "")}>
                        <i class="fa-solid fa-star text-amber-400"></i>
                    </div>
                </div>
            {/each}
            <p>500+</p>
        </div>
    </div>
</SectionWrapper>