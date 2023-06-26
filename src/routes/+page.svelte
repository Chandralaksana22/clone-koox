<script lang="ts">
    import ButtonGroup from "$lib/navigation/ButtonGroup.svelte";
    import SectionJuice from "$lib/home/SectionJuice.svelte";
    import SectionOrganic from "$lib/home/SectionOrganic.svelte";
    import Navbar from "$lib/navigation/Navbar.svelte";
    import SectionCold from "$lib/home/SectionCold.svelte";
    import SectionUnpasteurised from "$lib/home/SectionUnpasteurised.svelte";
    import SectionMenu from "$lib/home/SectionMenu.svelte";
    import Footer from "$lib/navigation/Footer.svelte";
</script>

<Navbar />
<section class="h-screen container mx-auto w-screen bg-white lg:container-lg">
    <div class="juice-farmacy">
        <SectionJuice />
        <SectionOrganic />
        <SectionCold />
        <SectionUnpasteurised />
        <SectionMenu />
    </div>
</section>
<ButtonGroup />
<Footer />
