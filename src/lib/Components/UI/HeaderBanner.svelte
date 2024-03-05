
<script>
import headerPicture from '$lib/assets/foto2.png';
import Header from './Header.svelte';
import Button from '$lib/Components/UI/Button.svelte';



$: headerStyle = `background-image: url(${headerPicture}); 
                height: 35rem;
                background-size: cover;
                padding-top: 2px;
                height: 100vh;
                width: 100vw;
         `

</script>




<style>
#bannerInfo{
       margin: 5rem;
       padding: 1rem;
       opacity: 99%;
       background-color: rgba(255, 255, 255, 0);
       margin-top: 10rem;
       display: flex;
       flex-direction: column;
       justify-content: space-between;
       width: 20rem;
       background-color: blue;
       flex-direction: column;
       
       
}


h1{
       margin-top: 5rem;
       color: aqua;}
</style>


<Header/>


<div id='headerBanner' style={headerStyle}>
       <div id = 'button-container'>
              
              <div id='bannerInfo'>
              <Button>Contact</Button>
              <Button>Nu bellen</Button>   
              <Button>Route</Button>      
              </div>
       </div>
</div>


