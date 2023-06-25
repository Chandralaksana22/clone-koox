<script lang="ts">
    import AOS from "aos";
    import { onMount, onDestroy } from "svelte";

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

<div
    class="h-screen flex flex-col lg:flex-row mt-10 mb-10"
    data-aos="fade-down"
>
    <div class="w-full lg:w-1/2">
        <img src="pisau.png" alt="Tomato" class="w-full z-20" />
    </div>
    <div class="w-full lg:w-1/2 flex flex-col justify-center items-center z-0">
        <div class="text-center text-[#225732]">
            <span class="text-md font-bold">. 04 .</span>
            <br />
            <span class="text-5xl">Unpasteurised</span>
            <br />
            <span class="text-5xl">No HPP</span>
        </div>
    </div>
</div>
