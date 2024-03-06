
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
                height: 35rem;
                background-size: cover;
                padding-top: 2px;
                height: 100vh;
                width: 100vw;
                flex-direction: ${mobile};
                overflow-y: scroll;
                
                
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
       margin: 5rem;
       padding: 1rem;
       opacity: 100%;
       background-color: rgba(255, 255, 255, 0);
       margin-top: 10rem;
       display: flex;
       height: 350px;
       width: 10rem;
       
       justify-content: space-around;
       flex-direction: column;
       
       
}

#headerBanner{
       display: flex;
       justify-content: space-evenly;
}

#card{
      
       
       display: flex;
       margin-top: 8rem;
       background-color: rgba(250, 235, 215, 0);
       height:  500px;
       width: 500px;
       justify-content: center;
       


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
              <Button>Services</Button>    
              <Button>Offerte Aanvragen</Button>        
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


