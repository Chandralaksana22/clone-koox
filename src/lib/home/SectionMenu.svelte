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
    function goToMenu() {
        window.location.href = "/menu";
    }
</script>

<div class="hero h-screen bg-transparent relative mt-10 mb-10">
    <img
        src="jeruk.png"
        class="absolute left-0 top-[60px] h-[92px] lg:h-[243px] w-auto"
        data-aos="fade-down"
    />
    <img
        src="daun-3.png"
        class="absolute right-0 top-[-30px] h-[208px] lg:h-[273px] w-auto"
        data-aos="fade-down"
    />
    <img
        src="abstrak-3.png"
        class="absolute bottom-[80px] left-[30%] transform -translate-x-1/2 h-[208px] lg:h-[273px] w-auto"
        data-aos="fade-down"
    />
    <img
        src="bawang.png"
        class="absolute bottom-[70px] right-[68%] lg:right-[34%] transform translate-x-1/2 h-[150px] lg:h-[273px] w-auto"
        data-aos="fade"
    />
    <img
        src="daun-5.png"
        class="absolute bottom-[50px] right-0 h-[150px] lg:h-[273px] w-auto"
        data-aos="fade-down"
    />
    <div class="hero-content text-center relative">
        <div class="w-full">
            <h1 class="text-[#225732] text-2xl lg:text-5xl md:text-4xl sm:text-2xl font-bold" data-aos="fade-down">
                Menu
            </h1>
            <p class="text-[#225732] text-md" data-aos="fade-down">
                Discover Now
            </p>
            <button
                class="btn btn-square btn-outline mt-5"
                style="color: #225732; border-color: #225732; background-color: transparent; transform: rotate(45deg);"
                on:click={goToMenu}
            >
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-6 w-6"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    ><path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M6 18L18 6M6 6l12 12"
                    /></svg
                >
            </button>
        </div>
    </div>
</div>
