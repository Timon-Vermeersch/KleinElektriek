
<script>

import { onMount, onDestroy } from "svelte";
import image1 from "$lib/assets/1-7.jpg"
import image2 from "$lib/assets/1-2.jpg"
import image3 from "$lib/assets/1-3.jpg"
import image4 from "$lib/assets/1-4.jpg"
import image5 from "$lib/assets/1-5.jpg"
import image6 from "$lib/assets/1-6.jpg"
import image7 from "$lib/assets/1-19.jfif"
import image8 from "$lib/assets/1-12.jfif"
import image9 from "$lib/assets/1-13.jfif"
import image10 from "$lib/assets/1-14.jfif"
import image11 from "$lib/assets/1-15.jfif"
import image12 from "$lib/assets/1-16.jfif"
import image13 from "$lib/assets/1-17.jfif"
import image14 from "$lib/assets/1-18.jfif"

let mainContainer;
    
    function scrollLeft() {
        if (mainContainer) {
          mainContainer.scrollBy({ left: -310, behavior: 'smooth' });
        }
    }
    function scrollRight() {
        if (mainContainer) {
          mainContainer.scrollBy({ left: 310, behavior: 'smooth' });
        }
    }

    function handleKeydown(event) {
        switch (event.key) {
            case 'ArrowLeft':
                scrollLeft();
                break;
            case 'ArrowRight':
                scrollRight();
                break;
        }
    }

    onMount(() => {
        window.addEventListener('keydown', handleKeydown);
    });

    onDestroy(() => {
        window.removeEventListener('keydown', handleKeydown);
    });
    
    

</script>

<style>
    #galleryContainer {
         position: relative; 
         overflow: hidden;
         max-width: 100svw;
    }
    #mainContainer{
        background-color: #E1771E;
        height: auto;
        position: relative;
        display: flex;
        justify-content: space;
        overflow: auto;
    }

    img{
        width: 20rem;
        height: 20rem;
        background-size: stretch;
        object-fit: cover;

    }
    div{
        
        background-color: #E1771E;
        justify-content: space-between;
        padding: 0.2rem;
    }
    p.thick {
  font-weight: bold;
  margin: 0;
  padding: 0;
}
p{
    margin: 0;
}
.arrow {
      cursor: pointer;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      z-index: 10; 
      font-size: 36px;
      background-color: #E1771E;
      border-radius: 12px;
      user-select: none;
    }
    
    .arrow.left {
      left: 0; 
    }
    
    .arrow.right {
      right: 0; 
    }

  
</style>
<!-- <div style="color:white;">{yScroll}</div> -->
<!-- bind:this={mainContainer} on:scroll={parseScroll} -->
<div id='galleryContainer'>
    <div id='mainContainer' bind:this={mainContainer} >
    
<!-- foto1 -->
    <div>
                
        <article><img src={image7} alt=""></article>
        
    </div>

<!-- foto2 -->

        <div>
            <article><img src={image2} alt=""></article>
            
        </div>

<!-- foto3 -->
   <div class='foto'>
    
    <article><img src={image3} alt=""></article>
   </div>

<!-- foto4 -->
        <div class='foto'>
            
            <article><img src={image9} alt=""></article>
            
        </div>
        <div class='foto'>
            
            <article><img src={image8} alt=""></article>
            
        </div>
        <div class='foto'>
            
            <article><img src={image10} alt=""></article>
            
        </div>
        <div class='foto'>
            
            <article><img src={image11} alt=""></article>
            
        </div>

        <div class='foto'>
            
            <article><img src={image13} alt=""></article>
            
        </div>
        <div class='foto'>
            
            <article><img src={image14} alt=""></article>
            
        </div>
        <div class='foto'>
                
            <article><img src={image12} alt=""></article>
            
        </div>
        <div class='foto'>
            <!-- <p class='thick'>TEXT</p>
            <p>subtext</p> -->
           <article><img src={image1} alt=""></article>
       </div>
        <div class='foto'>
            
            <article><img src={image4} alt=""></article>
            
        </div>
<!-- extra -->


        <div>
            
            <article><img src={image6} alt=""></article>
            
        </div>
        <div>
            
            <article><img src={image5} alt=""></article>
            
        </div>

</div>
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <span class="arrow left" on:click={scrollLeft}>&lt;</span>
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <span class="arrow right" on:click={scrollRight}>&gt;</span>
</div>


