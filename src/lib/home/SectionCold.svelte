<script lang="ts">
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

<section
    class="h-screen flex flex-col lg:flex-row-reverse lg:flex-row"
    data-aos="fade"
    data-aos-easing="linear"
    data-aos-duration="1500"
    style="height:100vh;"
>
    <div
        class="w-full lg:w-1/2 flex flex-col justify-center items-center"
        data-aos="fade"
        data-aos-easing="linear"
        data-aos-duration="1500"
    >
        <div class="text-center text-[#225732]">
            <span class="text-md font-bold">. 03 .</span>
            <br />
            <span class="text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                >cold</span
            >
            <br />
            <span class="text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                >pressed</span
            >
        </div>
    </div>
    <div
        class="w-full lg:w-1/2"
        data-aos="fade"
        data-aos-easing="linear"
        data-aos-duration="1500"
    >
        <img src="tomato.png" alt="Tomato" class="w-full z-20" />
    </div>
</section>
