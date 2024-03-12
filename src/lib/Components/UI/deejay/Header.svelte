<script>
    import Contact from './Contact.svelte';
    import CallNow from './CallNow.svelte';
    import { fade } from 'svelte/transition';
    $: innerWidth = 0
    

</script>

<svelte:window bind:innerWidth  />
<style>
  div {
    
    display: flex;
    position: fixed;
    width: 100vw;
    top: 0;
    left: 0;
    height: 3.5rem;
    background-color: #006d6d23;
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    /* opacity: 100; */
    
  }
  .title-container {
    
    flex-grow: 1;
    display: flex;
    justify-content: center;
    position: relative;
    
  }

  h1 {
    color: white;
    font-family: 'Montserrat', sans-serif;
    margin: 0;
    justify-content: center;
    text-shadow: 2px 2px 0px #000000;
    font-size: clamp(0px , 4vw,40px);
    
  }


  .right-section {
  
  display: flex;
  align-items: center;
  margin-right: 1rem;
  justify-content: flex-end;
  max-width: 200rem;
  
  
  
}
.header-icon {
  
  max-width: 75rem;
  height: 2rem; 
  margin-right: 1rem;
  filter: invert(100%);
  padding-left: 1rem;
 
}
</style>

<div transition:fade={{ delay: 0, duration: 50 }}>
  
  <img src="/outlet-svgrepo-com.svg" alt="Outlet Icon" class="header-icon" >
    
    <div class="title-container"><h1>Kleine Elektriciteitswerken Serge</h1></div>
    {#if innerWidth >= 1100}
      <div class = "right-section">
        <Contact/>
        <CallNow/>
    
      </div>
    {/if}
  
    </div>
  
  