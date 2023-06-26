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

<section class="h-screen flex flex-col lg:flex-row-reverse mt-10 mb-10">
    <div class="w-full lg:w-1/2 flex flex-col justify-center items-center">
        <div class="text-center"  data-aos="fade"
        data-aos-easing="linear"
        data-aos-duration="1500">
            <div class="text-center text-[#225732]">
                <h1 class="text-md font-bold">. 02 .</h1>
                <h1
                    class="text-2xl lg:text-5xl md:text-4xl sm:text-2xl font-bold"
                >
                    100% Organic
                </h1>
                <br /><br />
                <h1 class="text-2xl lg:text-5xl md:text-4xl sm:text-2xl">
                    Certified by
                </h1>
                <br />
                <h1 class="text-2xl lg:text-5xl md:text-4xl sm:text-2xl">
                    Soil <br /> Association
                </h1>
            </div>
        </div>
    </div>
    <div class="w-full lg:w-1/2">
        <img
            src="apel.png"
            alt="Gambar Apel"
             data-aos="fade"
        data-aos-easing="linear"
        data-aos-duration="1500"
            class="md:order-2 w-auto h-80 lg:h-auto object-cover mx-auto"
        />
    </div>
</section>
