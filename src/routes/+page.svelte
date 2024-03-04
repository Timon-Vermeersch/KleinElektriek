<script>
    import Header from '$lib/Components/UI/Header.svelte';
    import HeaderBanner from '$lib/Components/UI/HeaderBanner.svelte';
    import DisplayLower from "$lib/Components/UI/displayLower.svelte"
    
    

</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap');
  
    :global(body) {
        margin: 0;
        background-color: #d9d9d9;
        font-family: 'Montserrat', sans-serif;
        /* background-image: url('https://wallpapercave.com/wp/wp5119602.jpg'); */
        background-size: cover;
  }

</style>



<!-- <Header/> -->
<HeaderBanner/>

<DisplayLower/>

