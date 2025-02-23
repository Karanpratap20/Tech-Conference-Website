<script>
    export let index;
    export let speak;
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-14 lg:gap-20 relative text-base">
    <div class={"flex flex-col gap-8 md:gap-10"+ (index % 2 === 1 ? " md:order-2" : " ")}>
        <h4 class="text-2xl sm:text-3xl md:text:4xl max-w-[1000px] w-full font-medium relative pr-10 after:absolute after:top-full after:left-0 after:w-1/5 after:h-1.5 after:mt-1 after:bg-slate-900">
            <slot/>
        </h4>
        <p class="flex flex-col text-3xl text-semibold text-white">{speak.title}</p>
        <p class="flex flex-col text-xl text-white">{speak.bio}</p>
        <div class="flex items-center">
            <button class="specialBtnDark mr-auto font-semibold" on:click={() => window.open(speak.wiki, "_blank")}>
                <p>Know More &rarr;</p>
            </button>
        </div>
    </div>
    <div class={"flex flex-col dropShadow overflow-hidden rounded-b-lg"}>
        <div class="flex flex-col bg-white gap-4 flex-1">
            <img src={speak.img} alt="speaker-img">
        </div>
    </div>
</div>