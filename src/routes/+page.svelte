<script>
    import Header from '$lib/Components/UI/Header.svelte';
    import HeaderBanner from '$lib/Components/UI/HeaderBanner.svelte';
    import DisplayLower from "$lib/Components/UI/displayLower.svelte"
    import AboutCard from '$lib/Components/UI/AboutCard.svelte';
    import NuBellen from '$lib/Components/UI/NuBellen.svelte';
    import Choose from '$lib/Components/UI/ChooseGrid.svelte';
    import { onMount } from 'svelte';
    import DeejayHeaderbanner from '$lib/Components/UI/deejay/HeaderBanner.svelte';
    import DeejayDisplayLower from '$lib/Components/UI/deejay/displayLower.svelte';
    import Analytics from '$lib/Components/analytics.svelte'
    let site = 'home'

    function handeleSiteChange(event) {
        site = event.detail
    }


</script>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap');
  
    :global(body) {
        margin: 0;
        background-color: #d9d9d9;
        font-family: 'Montserrat', sans-serif;
        background-size: cover;
        overflow-y: none;
        max-width: 100%;
        font-weight: 900;
  }

</style>







<Analytics/>
{#if site === 'home'}
    <Choose on:changeSite={handeleSiteChange}/>
{:else if site === 'elek'}
    <HeaderBanner on:changeSite={handeleSiteChange}/>
    <DisplayLower/>
{:else if site === 'deejay'}
    <DeejayHeaderbanner on:changeSite={handeleSiteChange}/>
    <DeejayDisplayLower/>
{/if}


