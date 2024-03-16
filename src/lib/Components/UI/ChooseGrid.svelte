
<script>
    import {createEventDispatcher} from 'svelte'
    import image11 from "$lib/assets/11.jpg"
    import image2 from "$lib/assets/2.jpg"
    export let site;


  const dispatch = createEventDispatcher()

    function updateSite(newSite){
      site = newSite;
      dispatch('siteChange' , site);
    }





</script>

<svelte:head>
	<title>Kleine Elektriciteitswerken Serge </title>
    <meta name="description" content="Elektrische Diensten van Serge - uw lokale expert voor kleine elektriciteitsklussen. Snelle installatie en reparatie van stopcontacten, lichtarmaturen en meer. Neem contact op voor elektriciteitsvoorziening in uw poolhouse of voor het ophangen van een nieuw kader. Snel en betrouwbaar in uw regio.">
</svelte:head>


  
  <style>
    :global(html, body) {
      margin: 0;
      padding: 0;
      height: 100%;
      
    }
    
    :global(body) {

      background: linear-gradient(to right, #E1771E, #FFD080, #285A5C);
      color: white; 
    }
    
    .full-page-container {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      flex-wrap: wrap;
    }
    article{
      
      display: flex;
      justify-content: center;
      font-size: clamp(1rem, 1vw, 2rem); 
      display: flex;
      flex-direction: column;
      margin: 1.5rem;
      padding: 1rem;
      max-width: 40vw;
      max-height: 75vh;
      height: auto;
      width: 50rem;
      border: solid 1px black;
      cursor: pointer;
      
      
      
      
      
      

            /* From https://css.glass */
      background: rgba(255, 255, 255, 0.15);
      border-radius: 16px;
      box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
      backdrop-filter: blur(4.4px);
      -webkit-backdrop-filter: blur(4.4px);
      border: 1px solid rgba(255, 255, 255, 0.83);
    }


    .title{
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0.2rem;
      padding: 0.2rem;
      flex-wrap: wrap;  
    }
    .title h1{
      font-size: clamp(1rem, 2.5vw, 2rem); 
    }
    .card-img{
      padding: 0.5rem;
      margin: 0.5rem;
      display: flex;
      justify-content: center;
      height: 70%;
      max-height: 70%;
      max-width: 100%;
      overflow: hidden;
      display: block;
      
      
      /* object-fit: |tried| fill, contain, scale-down */
      
      
    }
    .card-img img{
      object-fit: cover; 
      width: 100%;
      height: 100%;
      border-radius: 30px;
      
      
      
    }
    .footer{
      margin: 0.4rem;
      padding: 0.1rem;
      display: flex;
      justify-content: center;
      text-shadow: 1px 2px 20px #000000;
      font-weight: 900;

    }
    
    .page-title {
    text-align: center;
    font-size: 2.5rem; 
    padding: 1rem;
    margin-bottom: 0.5rem; 
    color: #fff;
    }
    .cards-container{
      
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      
      
    }
    .first-article .card-img img{
      object-position: top center;
    }
    .second-article .card-img img {
      
    }

  </style>




  <div class = 'full-page-container'>
    <header>
      <h1 class="page-title">Welkom! Selecteer uw dienst.</h1>
    </header>
      <div class='cards-container'>
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
          <article class='first-article' on:click={() => {dispatch('changeSite' , 'deejay')}}>
            <div class='title'> <h1>Deejay Serge</h1></div>
            <div class='card-img'><img src="{image11}" alt="DeejaySerge"></div>
            <div class='footer'>Boek nu!</div>
          </article>  
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
          <article  class='second-article'on:click={() => {dispatch('changeSite' , 'elek')}}>  
            
            <div class='title'><h1>Kleine Elektriciteitswerken Serge</h1></div>
            <div class='card-img'><img src="{image2}" alt="DeejaySerge"></div>
            <div class='footer'>Schakel in!</div>

          </article>
      </div>
  </div>





