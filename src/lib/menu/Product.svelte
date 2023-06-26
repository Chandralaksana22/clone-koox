<script>
    let products = [
        {
            name: "Ultimate Detox",
            price: "£7.95",
            image: "https://koox.co.uk/data/wp-content/uploads/2018/05/Test_nico-575x1024.png",
            description: "Made with 100% organic ingredients",
            full_desct:
                "apple, lemon, celery, parsley, spinach, ale, ginger & nothing else Per 100mL: Energy 172kj (41kcal) - Fat 0.1 of which saturated 0.0 - Carbohydrates 9.2g of which sugar 9.0g - Fibre 0.7g - Protein 0.4g - Salt 0.02g",
        },
        {
            name: "Drinkable Skincare",
            price: "£7.95",
            image: "https://koox.co.uk/data/wp-content/uploads/2018/05/drinkable_skincare-575x1024.png",
            description: "Made with 100% organic ingredients",
            full_desct:
                "apple, lemon, celery, parsley, spinach, ale, ginger & nothing else Per 100mL: Energy 172kj (41kcal) - Fat 0.1 of which saturated 0.0 - Carbohydrates 9.2g of which sugar 9.0g - Fibre 0.7g - Protein 0.4g - Salt 0.02g",
        },
        {
            name: "Hydro Green",
            price: "£7.95",
            image: "https://koox.co.uk/data/wp-content/uploads/2018/05/GREEN_VITALITY-575x1024.png",
            description: "Made with 100% organic ingredients",
            full_desct:
                "apple, lemon, celery, parsley, spinach, ale, ginger & nothing else Per 100mL: Energy 172kj (41kcal) - Fat 0.1 of which saturated 0.0 - Carbohydrates 9.2g of which sugar 9.0g - Fibre 0.7g - Protein 0.4g - Salt 0.02g",
        },
    ];

    let activeProduct = null;

    function toggleDetail(product) {
        activeProduct = activeProduct === product ? null : product;
    }
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
    function goToMenu() {
        window.location.href = "/menu";
    }
</script>

<div class="product-container">
    {#each products as product}
        <section class="product-section">
            {#if activeProduct === product}
                <div class="detail active" data-aos="fade-in">
                    <div class="detail-content">
                        <div class="detail-info z-40">
                            <h3
                                class="product-name text-[#225732] text-sm lg:text-5xl md:text-4xl sm:text-2xl"
                            >
                                {product.name}
                            </h3>
                            <button
                                class="btn btn-square btn-outline mt-5"
                                style="color: #225732; border-color: #225732; background-color: transparent; transform: rotate(45deg);"
                                on:click={() => toggleDetail(product)}
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
                        <div
                            class="grid grid-cols-2 gap-4 place-content-center h-48"
                        >
                            <div
                                class="card w-72 bg-white text-neutral-content"
                            >
                                <div class="card-body items-center text-center">
                                    <h2 class="card-title text-[#225732]">
                                        {product.description}
                                    </h2>
                                    <p>{product.full_desct}</p>
                                </div>
                            </div>
                            <div
                                class="detail-image"
                                style="background-image: url({product.image})"
                            />
                        </div>
                    </div>
                </div>
            {:else}
                <div
                    class="product h-screen"
                    on:click={() => toggleDetail(product)}
                    data-aos="fade-down"
                >
                    <div class="product-info text-center">
                        <h3
                            class="product-name text-[#225732] text-sm lg:text-5xl md:text-4xl sm:text-2xl"
                        >
                            {product.name}
                        </h3>
                        <div class="button-container mx-auto">
                            <button
                                class="btn btn-square btn-outline mt-5"
                                style="color: #225732; border-color: #225732; background-color: transparent; transform: rotate(45deg);"
                                on:click={() => toggleDetail(product)}
                            >
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="h-6 w-6"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                    stroke="currentColor"
                                >
                                    <path
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M6 18L18 6M6 6l12 12"
                                    />
                                </svg>
                            </button>
                        </div>
                    </div>
                    <div
                        class="product-image"
                        style="background-image: url({product.image})"
                        data-aos="fade-down"
                    />
                </div>
            {/if}
        </section>
        <div class="container mx-auto flex flex-col md:hidden pt-24 pb-24">
            {#if activeProduct === product}
                <div class="detail active relative z-20">
                    <div class="detail-content" style="padding: 70px;">
                        <button
                            class="btn btn-square btn-outline absolute top-0 right-[10px] mt-5"
                            style="color: #225732; border-color: #225732; background-color: transparent; transform: rotate(45deg);"
                            on:click={() => toggleDetail(product)}
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                class="h-6 w-6"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke="currentColor"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    stroke-width="2"
                                    d="M6 18L18 6M6 6l12 12"
                                />
                            </svg>
                        </button>
                        <h3
                            class="product-name text-[#225732] mt-[70px] text-2xl lg:text-5xl md:text-4xl sm:text-2xl"
                        >
                            {product.name}
                        </h3>
                        <p
                            class="product-name text-[#225732] mt-[70px] text-md lg:text-5xl md:text-4xl sm:text-2xl"
                        >
                            {product.price}
                        </p>
                        <div
                            class="product-image-sm mx-auto"
                            style="background-image: url({product.image})"
                            data-aos="fade-down"
                        />
                        <div class="fixed bottom-0 inset-x-0 overflow-hidden">
                            <div class="w-screen bg-white h-10 mx-auto">
                                <h2 class="card-title text-sm text-center mx-auto p-3 text-[#225732]">
                                    {product.description}
                                  </h2>                                  
                            </div>
                          </div>
                          
                    </div>
                </div>
            {:else}
                <div class="flex flex-col items-center">
                    <h3
                        class="product-name text-[#225732] text-sm lg:text-5xl md:text-4xl sm:text-2xl"
                    >
                        {product.name}
                    </h3>
                    <div>
                        <button
                            class="btn btn-square btn-outline mt-10 mb-10"
                            style="color: #225732; border-color: #225732; background-color: transparent; transform: rotate(45deg);"
                            on:click={() => toggleDetail(product)}
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                class="h-6 w-6"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke="currentColor"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    stroke-width="2"
                                    d="M6 18L18 6M6 6l12 12"
                                />
                            </svg>
                        </button>
                    </div>
                    <div
                        class="product-image-sm mx-auto"
                        style="background-image: url({product.image})"
                        data-aos="fade-down"
                    />
                </div>
            {/if}
        </div>
    {/each}
</div>
