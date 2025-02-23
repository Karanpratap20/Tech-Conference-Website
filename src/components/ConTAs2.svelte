<script>
    import { goto } from "$app/navigation";

    function goToContact() {
        goto("/contact");
    }
</script>

<div class="flex item-center gap-4">
    <button on:click={goToContact} class="specialBtn">
        <p class="text-base sm:text-lg md:text-xl">Contact Us</p>
    </button>
    <button class={"specialBtnDark"}>
        <p class="text-base sm:text-lg md:text-xl">Register Now &rarr;</p>
    </button>
</div>