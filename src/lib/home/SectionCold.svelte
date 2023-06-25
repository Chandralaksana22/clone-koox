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

<div
    class="h-screen flex flex-col lg:flex-row"
    data-aos="fade-down"
    style="height:100vh;"
>
    <div class="w-full lg:w-1/2">
        <img src="tomato.png" alt="Tomato" class="w-full z-20" />
    </div>
    <div class="w-full lg:w-1/2 flex flex-col justify-center items-center">
        <div class="text-center text-[#225732]">
            <span class="text-md font-bold">. 03 .</span>
            <br />
            <span class="text-5xl">cold</span>
            <br />
            <span class="text-5xl">pressed</span>
        </div>
    </div>
</div>
