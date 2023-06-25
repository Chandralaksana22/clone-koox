<script>
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

<div class="h-screen flex flex-col lg:flex-row mt-10 mb-10">
    <div class="w-full lg:w-1/2">
        <img
            src="apel.png"
            alt="Gambar Apel"
            data-aos="fade-down"
            class="md:order-2"
        />
    </div>
    <div class="w-full lg:w-1/2 flex flex-col justify-center items-center">
        <div class="text-center" data-aos="fade-down">
            <div class="text-center text-[#225732]">
                <h1 class="text-md font-bold">. 02 .</h1>
                <h1 class="text-5xl font-bold">100% Organic</h1>
                <br /> <br />
                <h1 class="text-5xl">Certified by</h1>
                <br />
                <h1 class="text-5xl">Soil <br /> Association</h1>
            </div>
        </div>
    </div>
</div>
