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

<div class="hero h-screen bg-transparent relative mt-10 mb-10">
  <img
    src="daun.png"
    class="absolute left-0 top-[-50px] z-10 h-[243px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="daun-2.png"
    class="absolute left-1/2 transform -translate-x-1/2 top-[-20px] z-10 h-[243px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="daun-3.png"
    class="absolute right-0 top-[-30px] z-10 h-[273px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="kue.png"
    class="absolute left-[500px] transform -translate-x-1/2 top-0 z-10 h-[102px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="cup.png"
    class="absolute bottom-[70px] mt-5 left-[-88px] z-10 h-[273px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="daun-4.png"
    class="absolute left-[20%] transform -translate-x-1/2 bottom-[100px] z-10 h-[173px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="abstrak-3.png"
    class="absolute bottom-[80px] left-[30%] transform -translate-x-1/2 z-10 h-[273px] w-auto"
    data-aos="fade-down"
  />
  <img
    src="tomat.png"
    class="absolute bottom-[70px] right-[34%] transform translate-x-1/2 z-10 h-[150px] w-auto"
    data-aos="fade"
  />
  <img
    src="sendok.png"
    class="absolute bottom-[50px] right-0 z-10 h-[273px] w-auto"
    data-aos="fade-down"
  />
  <div class="hero-content text-center relative">
    <div class="w-full">
      <h1 class="text-[#225732] text-7xl font-bold" data-aos="fade-down">
        <img
          src="abstrak.png"
          alt="Abstrak"
          class="inline h-48 w-auto z-10"
          data-aos="fade-down"
        />
        Juice Farmacy
        <img
          src="abstrak-2.png"
          alt="Abstrak 2"
          class="inline h-48 w-auto z-10"
          data-aos="fade-down"
        />
      </h1>
    </div>
  </div>
</div>
