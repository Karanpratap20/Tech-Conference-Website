<script>
    import About from "../components/About.svelte";
    import Contact from "../components/Contact.svelte";
    import Conversion from "../components/conversion.svelte";
import Header from "../components/Header.svelte";
    import Hero from "../components/Hero.svelte";
    import Schedule from "../components/Schedule.svelte";
    import Speaker from "../components/Speaker.svelte";
    import Sponsor from "../components/Sponsor.svelte";
</script>


<main class="flex flex-col">
    <Header />
    <Hero />
    <Speaker/>
    <Schedule/>
    <Sponsor/>
    <About/>
    <Conversion/>
</main>