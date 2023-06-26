<script lang="ts">
    import ButtonGroup from "$lib/navigation/ButtonGroup.svelte";
    import Navbar from "$lib/navigation/Navbar.svelte";
    import Footer from "$lib/navigation/Footer.svelte";
    import AOS from "aos";
    import { onMount, onDestroy } from "svelte";
    import { fly } from "svelte/transition";

    let visible = true;

    onMount(() => {
        setTimeout(() => {
            AOS.refresh();
        }, 1000);
        setTimeout(() => {
            visible = false;
        }, 300);
    });

    onDestroy(() => {
        visible = true;
    });
</script>

<Navbar />
<section class="h-screen container mx-auto w-screen bg-white">
    <div class="juice-farmacy">
        <div class="hero h-screen bg-transparent">
            <div class="text-center">
                <div class="w-full h-screen pt-56">
                    <h1
                        class="text-[#225732] text-4xl lg:text-9xl md:text-4xl sm:text-2xl font-bold"
                        data-aos="fade"
                    >
                    100%
                    </h1>
                    <p  class="text-[#225732] text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                    data-aos="fade">
                    Organic <br>
                    Cold-pressed <br>
                    Raw
                    </p>
                </div>
            </div>
        </div>
        <div class="hero h-screen bg-transparent">
            <div class="text-center">
                <div class="w-full h-screen pt-56">
                    <h1
                        class="text-[#225732] text-4xl lg:text-9xl md:text-4xl sm:text-2xl font-bold"
                        data-aos="fade"
                    >
                   0%
                    </h1>
                    <p  class="text-[#225732] text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                    data-aos="fade">
                    Additives <br>
                    Pasteurisation <br>
                    HPP
                    </p>
                </div>
            </div>
        </div>
        <div class="hero h-screen bg-transparent">
            <div class="text-center">
                <div class="w-full h-screen pt-56">
                    <h1
                        class="text-[#225732] text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                        data-aos="fade"
                    >
                    IS THE WHITE SEDIMENT IN MY BOTTLE NORMAL?
                    </h1>
                    <br>
                    <br>
                    <p  class="text-[#225732] text-sm lg:text-5xl md:text-4xl sm:text-2xl"
                    data-aos="fade">
                    Yes ! The white sediment is the gingerol – ginger’s <br> bioactive compound. You will find it in the Ultimate Detox, <br> Dr. Green, Happy Gut and Shield Immunity. <br>
                    <br>
                    It is super good for you, so shake the bottle well
                    </p>
                </div>
            </div>
        </div>
    </div>
</section>
<ButtonGroup />
<Footer />
