
<script>
import Youtube from './deejay/youtube.svelte';
import headerPicture from '$lib/assets/foto222.png';
import Header from './Header.svelte';
import Button from '$lib/Components/UI/Button.svelte';
import MapsCard from './MapsCard.svelte';
import NuBellen from './NuBellen.svelte';
import AboutCard from './AboutCard.svelte';
import {createEventDispatcher} from 'svelte'
let mobile = ''
let state = 'about'
let scroll = ''
let scrolledY =0;
$: innerWidth = 0;
$: innerHeight = 0;
$: mobile = innerWidth < 1100 ? '' : '';
$: scroll = innerWidth < 1100 ? 'scroll': 'none'

const dispatch = createEventDispatcher()
const colorPalette = {
  darkestTeal: '#006d6d',
  mediumTeal: '#1d9a9a',
  lightTeal: '#3ac1c1',
  lightestTeal: '#54d8d8',
  brightestTeal: '#88efef'
};
 let site;
function handeleSiteChange(event) {
        site = event.detail
    }

$: headerStyle = `background-image: url(${headerPicture}); 
                
                background-size: cover;
                padding-top: 2px;
                min-height: 100svh;
                max-width: 100svw;
                flex-direction: ${mobile};
                
                display:flex;
                justify-content: center;
                align-items: center;
                flex-wrap: wrap;
                
                
                
                
                
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

function scrollToBottom() {
    const maxHeight = document.body.scrollHeight;
    window.scrollTo({top: maxHeight, behavior: 'smooth'});
  }
</script>
<svelte:window bind:innerWidth bind:innerHeight bind:scrollY={scrolledY} />



<style>
#bannerInfo{

       
       margin: 5rem 5rem 1rem 5rem; /* Top Right Bottom Left */
       padding: 1rem;
       opacity: 100%;
       background-color: rgba(255, 255, 255, 0);
       display: flex;
       
       width: 10rem;
       flex-direction: column;
       justify-content: space-evenly;
       gap: 1rem;
       
       
}

#headerBanner{
       
       display: flex;
       
       
       
}

#card{
              /* From https://css.glass */
              background: rgba(84, 216, 216, 0.24);
              border-radius: 16px;
              box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
              backdrop-filter: blur(7px);
              -webkit-backdrop-filter: blur(4.9px);
              border: 1px solid rgba(84, 216, 216, 0.9);
       
       display: flex;
       margin: 1rem;
       margin-top: 2rem;
       max-height:  28rem;
       justify-content: center;
       margin-left: 1rem;
       border-radius: 25px;
       border-style: solid ;
       border-width: 1.5px;
       overflow: hidden;
       max-width: 35rem;
       
       
       


}

h1{
       margin-top: 5rem;
       color: aqua;
       }
</style>


{#if (scrolledY < innerHeight * 0.1)}
<Header on:changeSite={() => {dispatch('changeSite' , 'home')}}/>
{/if}


<div id='headerBanner' style={headerStyle}>
       <div id = 'button-container'>
              
              <div id='bannerInfo'>
              <Button on:click = {setAbout}>Welkom</Button>
              <Button on:click = {setBellen}>Info</Button>   
              <Button on:click = {setRoute}>Route</Button>
              <Button on:click = {scrollToBottom}>Galerij</Button>
              <Button on:click = {() => {dispatch('changeSite' , 'deejay')}}>Deejay Serge</Button>
              
                 
                     
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


