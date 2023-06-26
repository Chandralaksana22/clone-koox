<script lang="ts">
    import ButtonGroup from "$lib/navigation/ButtonGroup.svelte";
    import Navbar from "$lib/navigation/Navbar.svelte";
    import Footer from "$lib/navigation/Footer.svelte";
    import AOS from "aos";
    import { onMount, onDestroy } from "svelte";
    import { fly } from "svelte/transition";

    let hoveredLink = null;

    onMount(() => {
        setTimeout(() => {
            AOS.refresh();
        }, 1000);
        document.body.style.overflow = "hidden"; // Menonaktifkan scroll
    });

    onDestroy(() => {
        hoveredLink = null;
        document.body.style.overflow = "auto"; // Mengaktifkan kembali scroll
    });
</script>

<Navbar />
<section class="h-screen container mx-auto w-screen bg-white">
    <div class="juice-farmacy">
        <div class="hero h-screen bg-transparent">
            <div class="text-center">
                <div class="w-full h-screen pt-56 flex flex-col items-center">
                    <a
                        href="https://www.ubereats.com/gb/feed?pl=JTdCJTIyYWRkcmVzcyUyMiUzQSUyMldDMUUlMjA3QlMlMjIlMkMlMjJyZWZlcmVuY2UlMjIlM0ElMjJDaElKVmYzSDJ5MGJka2dSSnBfUm1vRVNJVlUlMjIlMkMlMjJyZWZlcmVuY2VUeXBlJTIyJTNBJTIyZ29vZ2xlX3BsYWNlcyUyMiUyQyUyMmxhdGl0dWRlJTIyJTNBNTEuNTIwMDElMkMlMjJsb25naXR1ZGUlMjIlM0EtMC4xMzEyJTdE"
                        class="text-xl lg:text-9xl md:text-4xl sm:text-2xl font-bold link"
                        data-aos="fade-down"
                        class:selected={hoveredLink === 1}
                        on:mouseenter={() => (hoveredLink = 1)}
                        on:mouseleave={() => (hoveredLink = null)}
                    >
                        Uber Eats
                    </a><br />
                    <a
                        href="https://deliveroo.co.uk/brands/koox-juice-farmacy"
                        class="text-xl lg:text-9xl md:text-4xl sm:text-2xl font-bold link"
                        data-aos="fade-down"
                        class:selected={hoveredLink === 2}
                        on:mouseenter={() => (hoveredLink = 2)}
                        on:mouseleave={() => (hoveredLink = null)}
                    >
                        Deliveroo
                    </a> <br />
                    <a
                        href="https://www.just-eat.co.uk/"
                        class="text-xl lg:text-9xl md:text-4xl sm:text-2xl font-bold link"
                        data-aos="fade-down"
                        class:selected={hoveredLink === 3}
                        on:mouseenter={() => (hoveredLink = 3)}
                        on:mouseleave={() => (hoveredLink = null)}
                    >
                        Just Eat
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>
<ButtonGroup />
<Footer />

<style>
    :global(.link) {
        color: #225732;
        text-decoration: none;
        transition: color 0.3s, opacity 0.3s;
        opacity: 1;
    }

    :global(.link:hover),
    :global(.link.selected) {
        color: #225732;
        opacity: 1;
    }

    :global(.link:not(:hover)) {
        color: #bdc2be;
        opacity: 0.7;
    }
</style>
