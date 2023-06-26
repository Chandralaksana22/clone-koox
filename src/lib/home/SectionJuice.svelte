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

<section class="hero h-screen bg-transparent relative mt-10 mb-10">
  <div
    class="absolute top-[8px] lg:top-0 left-0 w-full grid grid-cols-4 gap-4 z-10"
    data-aos="slide-down"
    data-aos-easing="linear"
   
  >
    <div>
      <img
        src="daun.png"
        class="z-10 h-auto lg:h-[243px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="daun-2.png"
        class="z-10 h-auto lg:h-[243px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="kue.png"
        class="z-10 h-auto lg:h-[102px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="daun-3.png"
        class="z-10 h-auto lg:h-[273px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
  </div>
  <div class="hero-content text-center relative">
    <div class="w-full flex justify-center">
      <h1
        class="text-[#225732] text-2xl lg:text-7xl md:text-4xl sm:text-2xl font-bold"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      >
        <img
          src="abstrak.png"
          alt="Abstrak"
          class="inline h-16 lg:h-48 w-auto z-10"
          data-aos="slide-down"
          data-aos-easing="linear"
         
        />
        Juice Farmacy
        <img
          src="abstrak-2.png"
          alt="Abstrak 2"
          class="inline h-16 lg:h-48 w-auto z-10"
          data-aos="slide-down"
          data-aos-easing="linear"
         
        />
      </h1>
    </div>
  </div>
  <div
    class="absolute bottom-[50px] lg:bottom-0 left-0 w-full grid grid-cols-5 gap-4 z-10"
    data-aos="slide-down"
  >
    <div>
      <img
        src="cup.png"
        class="z-10 h-auto lg:h-[273px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="daun-4.png"
        class="z-10 h-auto lg:h-[173px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="abstrak-3.png"
        class="z-10 h-auto lg:h-[273px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="daun.png"
        class="z-10 h-auto lg:h-[102px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
    <div>
      <img
        src="sendok.png"
        class="z-10 h-auto lg:h-[273px] w-auto"
        data-aos="slide-down"
        data-aos-easing="linear"
       
      />
    </div>
  </div>
</section>
