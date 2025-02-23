<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import SpeakerCard from "./SpeakerCard.svelte";
    let speaker = [
    { 
        name: "Elon Musk", 
        title: "CEO, Tesla & SpaceX", 
        img: "assets/elon.jpg",
        bio: "Elon Musk is a business magnate, investor, and engineer known for founding SpaceX, Tesla, Neuralink, and The Boring Company.",
        wiki: "https://en.wikipedia.org/wiki/Elon_Musk"
    },
    { 
        name: "Sundar Pichai", 
        title: "CEO, Google", 
        img: "assets/sundar.jpg",
        bio: "Sundar Pichai is the CEO of Alphabet Inc. and its subsidiary Google, known for his leadership in AI and cloud computing.",
        wiki: "https://en.wikipedia.org/wiki/Sundar_Pichai"
    },
    { 
        name: "Satya Nadella", 
        title: "CEO, Microsoft", 
        img: "assets/satya.jpg",
        bio: "Satya Nadella is an Indian-American business executive, serving as the CEO of Microsoft since 2014.",
        wiki: "https://en.wikipedia.org/wiki/Satya_Nadella"
    },
    { 
        name: "Sam Altman", 
        title: "CEO, OpenAI", 
        img: "assets/sam.jpg",
        bio: "Sam Altman is an entrepreneur and investor, known for leading OpenAI and formerly serving as the president of Y Combinator.",
        wiki: "https://en.wikipedia.org/wiki/Sam_Altman"
    },
    { 
        name: "Mark Zuckerberg", 
        title: "CEO, Meta", 
        img: "assets/mark.jpg",
        bio: "Mark Zuckerberg is the co-founder and CEO of Meta (formerly Facebook), a pioneer in social networking and the metaverse.",
        wiki: "https://en.wikipedia.org/wiki/Mark_Zuckerberg"
    },
    { 
        name: "Tim Cook", 
        title: "CEO, Apple", 
        img: "assets/tim.jpg",
        bio: "Tim Cook is the CEO of Apple, responsible for leading the company into new product innovations and sustainability efforts.",
        wiki: "https://en.wikipedia.org/wiki/Tim_Cook"
    }
];


</script>
<SectionWrapper id="Speaker">
    <div class="relative bg-[#181b34] rounded-xl p-8 mr-10 ml-10 shadow-lg dropShadow">
        <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
            <div class="flex flex-col gap-2">
                <p class="opacity-60 text-base sm:text-lg md:text-xl text-center text-white">
                    Start your <span class="text-indigo-600">journey</span> with the best in the industry.
                </p>
                <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center text-white">
                    Speakers for the Conference
                </h3>
            </div>
            {#each speaker as speak,index}
                <SpeakerCard {speak} {index}>
                    {#if index==0}
                    <span class="text-indigo-500 text-6xl font-semibold">Elon Musk</span>
                    {:else if index==1}
                    <span class="text-indigo-500 text-6xl font-semibold">Sundar Pichai</span>
                    {:else if index==2}
                    <span class="text-indigo-500 text-6xl font-semibold">Satya Nadella</span>
                    {:else if index==3}
                    <span class="text-indigo-500 text-6xl font-semibold">Sam Altman</span>
                    {:else if index==4}
                    <span class="text-indigo-500 text-6xl font-semibold">Mark Zuck</span>
                    {:else if index==5}
                    <span class="text-indigo-500 text-6xl font-semibold">Tim Cook</span>
                    {/if}
                </SpeakerCard>
            {/each}
        </div>
    </div>
</SectionWrapper>