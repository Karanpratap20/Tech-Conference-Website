<script>
    import ScheduleCard from "./ScheduleCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";

    let lim=true
    
    let schedulelist = [
        {
            speaker: "Elon Musk",
            date: "March 15, 2025",
            time: "10:00 AM - 11:30 AM",
            topic: "The Future of Space Travel & AI",
            description: "Exploring the potential of AI-driven space exploration, interplanetary travel, and SpaceX’s vision for Mars colonization.",
            img: "assets/elon.jpg"
        },
        {
            speaker: "Sundar Pichai",
            date: "March 15, 2025",
            time: "12:00 PM - 1:30 PM",
            topic: "AI, Search, and the Evolution of Google",
            description: "How AI is transforming Google Search, the role of Large Language Models, and the ethical implications of AI-driven search engines.",
            img: "assets/sundar.jpg"
        },
        {
            speaker: "Satya Nadella",
            date: "March 16, 2025",
            time: "10:00 AM - 11:30 AM",
            topic: "Cloud Computing & The Next Digital Revolution",
            description: "Discussing the rise of cloud computing, AI integration in business, and the future of quantum and edge computing.",
            img: "assets/satya.jpg"
        },
        {
            speaker: "Sam Altman",
            date: "March 16, 2025",
            time: "12:00 PM - 1:30 PM",
            topic: "Artificial General Intelligence & Ethical AI",
            description: "The journey from Narrow AI to AGI, OpenAI’s research, and the challenges of developing ethical and responsible AI.",
            img: "assets/sam.jpg"
        },
        {
            speaker: "Mark Zuckerberg",
            date: "March 17, 2025",
            time: "10:00 AM - 11:30 AM",
            topic: "Metaverse & The Future of Social Media",
            description: "How VR, AR, and AI are shaping the Metaverse, the future of digital interactions, and privacy concerns in a virtual world.",
            img: "assets/mark.jpg"
        },
        {
            speaker: "Tim Cook",
            date: "March 17, 2025",
            time: "1:00 PM - 2:30 PM",
            topic: "Sustainability & The Future of Apple",
            description: "How Apple is innovating in sustainability, privacy, and accessibility, along with its future technology roadmap.",
            img: "assets/tim.jpg"
        }
    ];
</script>
<SectionWrapper id="Schedule">
    <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">Get ready to buy some time</p>
            <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                <span class="text-indigo-400">Itinerary</span> of Insights: Stay Ahead
            </h3>
        </div>
        <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
            <div class="flex flex-col gap-8">
                {#each lim ? schedulelist.slice(0,2) : schedulelist as schedule,index}
                    <ScheduleCard {schedule} left={true} {index}/>
                {/each}
            </div>
            <div class="w-[1px] bg-slate-950 hidden md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? schedulelist.slice(0,2) : schedulelist as schedule,index}
                    <ScheduleCard {schedule} {index}/>
                {/each}
            </div>
        </div>
        <button on:click={() => lim = !lim} class="specialBtn">
            <p>{lim ? 'Show All':'Show less'}</p>
        </button>
    </div>
</SectionWrapper>