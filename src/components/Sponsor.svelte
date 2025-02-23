<script>
    import ConTAs from "./ConTAs.svelte";

    let sponsors = [
        { img: "assets/sponsor/apple.png", url: "https://www.apple.com" },
        { img: "assets/sponsor/google.jpg", url: "https://www.google.com" },
        { img: "assets/sponsor/microsoft.png", url: "https://www.microsoft.com" },
        { img: "assets/sponsor/amazon.png", url: "https://www.amazon.com" },
        { img: "assets/sponsor/facebook.jpeg", url: "https://www.facebook.com" },
        { img: "assets/sponsor/tesla.png", url: "https://www.tesla.com" },
        { img: "assets/sponsor/nvidia.jpeg", url: "https://www.nvidia.com" },
        { img: "assets/sponsor/samsung.png", url: "https://www.samsung.com" },
        { img: "assets/sponsor/sony.png", url: "https://www.sony.com" },
        { img: "assets/sponsor/intel.png", url: "https://www.intel.com" },
        { img: "assets/sponsor/ibm.png", url: "https://www.ibm.com" },
        { img: "assets/sponsor/cisco.png", url: "https://www.cisco.com" },
        { img: "assets/sponsor/oracle.png", url: "https://www.oracle.com" },
        { img: "assets/sponsor/hp.png", url: "https://www.hp.com" },
        { img: "assets/sponsor/dell.jpg", url: "https://www.dell.com" },
        { img: "assets/sponsor/lg.jpeg", url: "https://www.lg.com" }
    ];

    let infiniteSponsors = [...sponsors, ...sponsors]; 
</script>

<style>
    .scroll-container {
        overflow: hidden;
        white-space: nowrap;
        position: relative;
        width: 100%;
    }

    .scroll-content {
        display: flex;
        align-items: center;
        animation: scroll 15s linear infinite;
    }

    .scroll-content a {
        margin: 0 16px;
        flex-shrink: 0;
    }

    .scroll-content img {
        height: 64px;
        width: auto;
        object-fit: contain;
        transition: transform 0.3s ease;
    }

    .scroll-content img:hover {
        transform: scale(1.1);
    }

    .scroll-content:hover {
        animation-play-state: paused;
    }

    @keyframes scroll {
        from {
            transform: translateX(0);
        }
        to {
            transform: translateX(-100%);
        }
    }
</style>

<section class="bg-black py-10">
    <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center text-white">
        FEATURED SPONSORS
    </h3>
    <div class="scroll-container max-w-[900px] mx-auto w-full py-10">
        <h2 class="text-center text-2xl font-semibold mb-6 text-white">
            Trusted by the <span class="text-indigo-400">Best</span>, Built for the <span class="text-green-400">Future</span>.
        </h2>
        <div class="scroll-content">
            {#each infiniteSponsors as sponsor}
                <a href={sponsor.url} target="_blank" rel="noopener noreferrer">
                    <img src={sponsor.img} alt={sponsor.img.split('/').pop().split('.')[0]}/>
                </a>
            {/each}
        </div>
    </div>
</section>
