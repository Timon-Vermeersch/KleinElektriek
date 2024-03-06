
<script>
import headerPicture from '$lib/assets/foto2.png';
import Header from './Header.svelte';
import Button from '$lib/Components/UI/Button.svelte';
import MapsCard from './MapsCard.svelte';
import NuBellen from './NuBellen.svelte';
import AboutCard from './AboutCard.svelte';
let mobile = ''
let state = 'about'
let scroll = ''
$: innerWidth = 0

$: mobile = innerWidth < 1100 ? '' : '';
$: scroll = innerWidth < 1100 ? 'scroll': 'none'





$: headerStyle = `background-image: url(${headerPicture}); 
                height: 30rem;
                background-size: cover;
                padding-top: 2px;
                height: 100vh;
                width: 100vw;
                flex-direction: ${mobile};
                overflow-y: scroll;
                display:flex;
                justify-content: center;
                align-items: center;
                
                
                
         `

function setAbout (){
       state = 'about'
}
function setRoute (){
       state = 'route'
}
function setBellen (){
       state = 'bellen'
}
</script>
<svelte:window bind:innerWidth  />



<style>
#bannerInfo{
       margin: 5rem 1rem 5rem 5rem; /* Top Right Bottom Left */
       padding: 1rem;
       opacity: 100%;
       background-color: rgba(255, 255, 255, 0);
       margin-top: 10rem;
       display: flex;
       height: 12px;
       width: 10rem;
       flex-direction: column;
       justify-content: space-evenly;
       gap: 1rem;
       
       
}

#headerBanner{
       display: flex;
       
       
}

#card{
      
       
       display: flex;
       margin-top: 1rem;
       background-color: rgba(250, 235, 215, 0.866);
       height:  30rem;
       justify-content: center;
       margin-left: 1rem;
       border-radius: 25px;
       


}

h1{
       margin-top: 5rem;
       color: aqua;
       }
</style>


<Header/>


<div id='headerBanner' style={headerStyle}>
       <div id = 'button-container'>
              
              <div id='bannerInfo'>
              <Button on:click = {setAbout}>Welkom</Button>
              <Button on:click = {setBellen}>Nu bellen</Button>   
              <Button on:click = {setRoute}>Route</Button>
              <Button>Contact</Button>  
                 
                     
              </div>
       </div>

       <div id = 'card'>
              
              {#if state == "about"}
              <AboutCard/>
              {:else if state == "route"}
              <MapsCard/>
              {:else if state == "bellen"}
              <NuBellen/>
              {/if}
       </div>
</div>


