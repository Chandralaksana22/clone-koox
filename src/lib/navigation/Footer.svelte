<script>
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

{#if isMenuOpen}
    <div class="menu-btn">
        <div class="menu-content">
            <ul> 
                <li><a href="/about" data-sveltekit-reload class="text-2xl text-[#225732]">About</a></li>
                <li><a href="/menu" data-sveltekit-reload class="text-2xl text-[#225732]">Menu</a></li>
                <li class="text-sm text-[#225732]">Cold-pressed</li>
                <li class="text-sm text-[#225732]">smoohies</li>
                <li class="text-sm text-[#225732]">boosters</li>
                <li class="text-sm text-[#225732]">bowls</li>
                <li class="text-sm text-[#225732]">treats</li>
                <li><a href="/order" data-sveltekit-reload class="text-2xl text-[#225732]">Order Now</a></li>
                <li><a href="/contact" data-sveltekit-reload class="text-2xl text-[#225732]">Contact</a></li>
            </ul>
        </div>
    </div>
{/if}

<footer
    class="footer items-center p-4 bg-white text-neutral-content hidden lg:flex"
>
    <div class="items-center grid-flow-col pl-14 text-black">
        <p>© 2021 Dark Points Network LTD • Credits • Legals</p>
    </div>
</footer>
<div class="footer footer-btn z-10">
    <button
        class="button footer-button lg:hidden mx-auto"
        on:click={toggleMenu}
    >
        <div class={isMenuOpen ? "cross" : "lines"} />
    </button>
</div>
