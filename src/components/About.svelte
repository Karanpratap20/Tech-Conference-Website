<script>
    import ConTAs from "./ConTAs.svelte";
import SectionWrapper from "./SectionWrapper.svelte";

</script>
<SectionWrapper id="about">
    <div class="relative rounded-xl p-8 m-1 shadow-lg dropShadow bg-white mt-20">
        <div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14">
            <div class="flex flex-col gap-2">
                <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                    Pioneering the Future of Technology & Innovation.
                </p>
                <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">
                    About TechElevate
                </h3>
            </div>
    
            <div class="max-w-4xl text-center text-lg sm:text-xl opacity-80 leading-relaxed">
                <p>
                    TechElevate is the premier tech conference bringing together visionaries, 
                    industry leaders, and innovators to explore the next frontier of technology. 
                    From groundbreaking advancements in AI and blockchain to the latest trends in cybersecurity, 
                    TechElevate is where the future takes shape.
                </p>
                <p class="mt-6">
                    Whether you're a developer, entrepreneur, or tech enthusiast, our event offers an 
                    unparalleled opportunity to connect, learn, and collaborate with the best minds in the industry. 
                    Join us as we shape the digital world of tomorrow.
                </p>
            </div>
    
            <div class="flex flex-wrap justify-center gap-6 mt-10">
                <div class="p-6 rounded-lg shadow-md bg-indigo-50 w-64 text-center">
                    <h4 class="text-xl font-semibold text-indigo-600">5000+ Attendees</h4>
                    <p class="opacity-70 text-sm mt-2">Engage with tech enthusiasts & experts from around the world.</p>
                </div>
                <div class="p-6 rounded-lg shadow-md bg-indigo-50 w-64 text-center">
                    <h4 class="text-xl font-semibold text-indigo-600">50+ Keynote Speakers</h4>
                    <p class="opacity-70 text-sm mt-2">Learn from the top minds in technology and innovation.</p>
                </div>
                <div class="p-6 rounded-lg shadow-md bg-indigo-50 w-64 text-center">
                    <h4 class="text-xl font-semibold text-indigo-600">100+ Exhibitors</h4>
                    <p class="opacity-70 text-sm mt-2">Experience hands-on demos of cutting-edge tech solutions.</p>
                </div>
            </div>
        </div>
    </div>
    
</SectionWrapper>