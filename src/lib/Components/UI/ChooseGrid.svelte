
<script>
    import image11 from "$lib/assets/11.jpg"
    import image2 from "$lib/assets/2.jpg"
	  // import ChooseItem from "$lib/Components/UI/deejay/ChooseItem.svelte";

    // let cards = [

    //     {id:'1', img:image11 , intro: 'This card will guide you to Deejay Serge'},
    //     {id:'2' ,img:image2, intro: 'This card will guide you to Kleine elektriciteitswerkenSerge'}

    // ]




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
      overflow: hidden;
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
      flex-direction: column;
      margin: 2rem;
      max-width: 60vw;
      max-height: 70vh;
      height: 50rem;
      width: 50rem;
      border: solid 1px black;
      

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
      margin: 0.5rem;
      padding: 0.5rem;
    }
    .card-img{
      margin: 0.5rem;
      display: flex;
      justify-content: center;
      max-height: 100%;
      max-width: 100%;
      overflow: hidden;
      display: block;
      border-radius: 30px;
      /* object-fit: |tried| fill, contain, scale-down */
      
      
    }
    .card-img img{
      object-fit: cover; 
      width: 100%;
      height: 100%;
      
    }
    .footer{
      margin: 0.5rem;
      padding: 0.5rem;
      display: flex;
      justify-content: center;

    }
    .page-title {
    text-align: center;
    font-size: 2.5rem; 
    margin-bottom: 2rem; 
    color: #fff;
    }
    .cards-container{
      display: flex;
      flex-direction: row;
    }

  </style>

<div class = 'full-page-container'>
      <header>
        <h1 class="page-title">Welkom! Selecteer uw dienst.</h1>
      </header>
 
      <div class='cards-container'>


        <article>
          <div class='title'> <h1>Deejay Serge</h1></div>
          <div class='card-img'><img src="{image11}" alt="DeejaySerge"></div>
          <!-- <div class='footer'>footer</div> -->
        </article>  
        
        <article>  
          
          <div class='title'><h1>Kleine Elektriciteitswerken Serge</h1></div>
          <div class='card-img'><img src="{image2}" alt="DeejaySerge"></div>
          <!-- <div class='footer'>This card will guide you to Kleine elektriciteitswerkenSerge</div> -->

        </article>

      </div>


 </div>
  
