<script>
    import Contact from './Contact.svelte';
    import CallNow from './CallNow.svelte';
    

</script>
<style>
  header {
    display: flex;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    height: 3rem;
    background-color: #305b4c;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.26);
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
  }
  .right-section {
  display: flex;
  align-items: center;
  margin-right: 1rem;
}
.header-icon {
  height: 2rem; 
  margin-right: 1rem;
  filter: invert(100%);
  padding-left: 1rem;
 
}
</style>

<header>
<img src="/outlet-svgrepo-com.svg" alt="Outlet Icon" class="header-icon" >
  
  <div class="title-container"><h1>Kleine Elektriciteitswerken Serge</h1></div>
  
    <div class = "right-section">
      <Contact/>
      <CallNow/>
    </div>


</header>
