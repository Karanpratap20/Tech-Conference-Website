<script>
  import "../app.css";
  import ConTAs from "../components/ConTAs.svelte";
  import ConTAs2 from "../components/ConTAs2.svelte";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";

  import { openModal } from "../store";

  let y;
  $: outerHeight = 0;

  function reroute(href) {
    $openModal = false;
    
    if (window.location.pathname === "/contact") {
      window.location.href = "/" + href;
    } else {
      window.location.href = href;
    }
  }
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 p-5 px-8 md:hidden"
  >
    <div class="flex items-center justify-between gap-4 border-b pb-2">
      <h1 class="text-lg font-semibold">
        <span class="text-black">TECH </span><span class="text-indigo-400"
          >ELEVATE</span
        >
      </h1>
      <!-- svelte-ignore event_directive_deprecated -->
      <button
        on:click={() => ($openModal = false)}
        class="outline-none border-none"
        aria-label="Close Menu"
      >
        <i class="fa-solid fa-xmark text-2xl"></i>
      </button>
    </div>
    <div class="flex flex-col gap-4 flex-1">
      <button on:click={() => reroute('#Speaker')} class="border-none outline-none p-2 group duration-200 cursor-pointer text-left">
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">Speaker <i class="fa-solid fa-chevron-right text-xl pl-4"></i></p>
      </button>
      <button on:click={() => reroute('#Schedule')} class="border-none outline-none p-2 group duration-200 cursor-pointer text-left">
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">Schedule <i class="fa-solid fa-chevron-right text-xl pl-4"></i></p>
      </button>
      <button on:click={() => reroute('#about')} class="border-none outline-none p-2 group duration-200 cursor-pointer text-left">
        <p class="duration-200 group-hover:pl-2 poppins text-3xl font-semibold">About <i class="fa-solid fa-chevron-right text-xl pl-4"></i></p>
      </button>
    </div>
    <div class="flex flex-col items-center justify-center">
      <ConTAs2 />
    </div>
  </div>
{/if}

{#if y > outerHeight}
  <div class="bg-[#181b34] bg-opacity-50 fixed top-0 left-0 w-full flex flex-col z-20 px-4 fadeIn">
      <Header/>
  </div>
{/if}

<slot />
<Footer />

<svelte:window bind:scrollY={y} bind:outerHeight />