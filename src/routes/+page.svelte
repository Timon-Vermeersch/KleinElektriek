<script>
    import Header from '$lib/Components/UI/Header.svelte';
    import HeaderBanner from '$lib/Components/UI/HeaderBanner.svelte';
    import DisplayLower from "$lib/Components/UI/displayLower.svelte"
    import AboutCard from '$lib/Components/UI/AboutCard.svelte';
    import NuBellen from '$lib/Components/UI/NuBellen.svelte';
    


</script>
<svelte:head>
	<title>Kleine Elektriciteitswerken Serge </title>
    <meta name="description" content="Elektrotechnische Diensten van Serge - uw lokale expert voor kleine elektriciteitsklussen. Snelle installatie en reparatie van stopcontacten, lichtarmaturen en meer. Neem contact op voor elektriciteitsvoorziening in uw poolhouse of voor het ophangen van een nieuw kader. Snel en betrouwbaar in uw regio.">


</svelte:head>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap');
  
    :global(body) {
        margin: 0;
        background-color: #d9d9d9;
        font-family: 'Montserrat', sans-serif;
        background-size: cover;
        overflow-y: none;
        max-width: 100%;
  }

</style>



<!-- <Header/> -->


<HeaderBanner/>


<DisplayLower/>



