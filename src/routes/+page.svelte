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
    let site = 'home'

    function handeleSiteChange(event) {
        site = event.detail
    }

    onMount(() => {
    // Create a script element for Google Analytics
    const script = document.createElement('script');
    script.src = 'https://www.googletagmanager.com/gtag/js?id=G-N3R3NZT5VK';
    script.async = true;
    document.head.appendChild(script);

    // Initialize Google Analytics after the script is loaded
    script.onload = () => {
      window.dataLayer = window.dataLayer || [];
      function gtag() { dataLayer.push(arguments); }
      gtag('js', new Date());
      gtag('config', 'G-N3R3NZT5VK');
    };
  });

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








{#if site === 'home'}
    <Choose on:changeSite={handeleSiteChange}/>
{:else if site === 'elek'}
    <HeaderBanner on:changeSite={handeleSiteChange}/>
    <DisplayLower/>
{:else if site === 'deejay'}
    <DeejayHeaderbanner on:changeSite={handeleSiteChange}/>
    <DeejayDisplayLower/>
{/if}


