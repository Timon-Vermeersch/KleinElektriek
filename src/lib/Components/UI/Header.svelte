<script>
    import Contact from './Contact.svelte';
    import CallNow from './CallNow.svelte';
    

</script>
<style>
  div {
    display: flex;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    height: 5rem;
    background-color: #30545b00;
    display: flex;
    justify-content: space-between;
    align-items: center;
    opacity: 100;
    
  }
  .title-container {
    flex-grow: 1;
    display: flex;
    justify-content: left;
    position: relative;
  }

  h1 {
    color: white;
    font-family: 'Montserrat', sans-serif;
    margin: 0;
    justify-content: center;
  }
  .right-section {
  display: flex;
  align-items: center;
  margin-right: 1rem;
  justify-content: flex-end;
  background-color: rgba(255, 255, 255, 0.201);
  
}
.header-icon {
  height: 2rem; 
  margin-right: 1rem;
  filter: invert(100%);
  padding-left: 1rem;
 
}
</style>

<div>
<img src="/outlet-svgrepo-com.svg" alt="Outlet Icon" class="header-icon" >
  
  <div class="title-container"><h1>Kleine Elektriciteitswerken Serge</h1></div>
  
    <div class = "right-section">
      <Contact/>
      <CallNow/>
    </div>


  </div>

