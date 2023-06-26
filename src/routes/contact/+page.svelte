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
                <div class="w-full h-screen pt-60 text-[#225732] flex flex-col items-center">
                    <a  href="mailto:contact@koox.co.uk"
                        class="text-sm lg:text-6xl md:text-4xl sm:text-2xl"
                        data-aos="fade"
                       
                    >
                    contact@koox.co.uk
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>
<ButtonGroup />
<Footer />

