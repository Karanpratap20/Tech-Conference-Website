<script>
    import { openModal } from "../store";
    
</script>

<header class="flex flex-col relative z-20 bg-[#181b34]">
    <div class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6">
        <a href="/">
            <h1 class="text-lg font-semibold"><span class="text-white">TECH </span><span class="text-indigo-400">ELEVATE</span></h1>
        </a>
        <button on:click={()=> $openModal = true} class="md:hidden grid place-items-center" aria-label="Open Menu">
            <i class="fa-solid fa-bars"></i>
        </button>
        <nav class="hidden md:flex item-center gap-4 lg:gap-6">
            <a href="#Speaker" class="duration-200 text-white hover:text-indigo-400 cursor-pointer mt-3">Speaker</a>
            <a href="#Schedule" class="duration-200 text-white hover:text-indigo-400 cursor-pointer mt-3">Schedule</a>
            <a href="#about" class="duration-200 text-white hover:text-indigo-400 cursor-pointer mt-3">About</a>
            <a href="#contact" class="duration-200 text-white hover:text-indigo-400 cursor-pointer mt-3">Contact</a>
            <button class="border-[#181b64]">
                <p>Login</p>
            </button>
        </nav>
    </div>
</header>