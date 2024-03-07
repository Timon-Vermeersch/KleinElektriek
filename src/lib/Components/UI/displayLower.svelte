
<script>

import { onMount } from "svelte";
import image1 from "$lib/assets/1.jpg"
import image2 from "$lib/assets/2.jpg"
import image3 from "$lib/assets/3.jpg"
import image4 from "$lib/assets/4.jpg"
import image5 from "$lib/assets/5.jpg"
import image6 from "$lib/assets/6.jpg"

// https://svelte.dev/repl/97366319dc7c477989fe744d01d81391?version=3.39.0


// $: mainContainer;
// $:  yScroll = 0;


// function parseScroll() {
//     yScroll = mainContainer.scrollTop;
// }

// onMount(() => {
//     mainContainer.addEventListener('scroll', parseScroll);
// });

</script>

<style>
    #mainContainer{
        background-color: #333333;
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
        /* padding: 1rem; */
        background-color: #333333;
        justify-content: space-between;
        padding: 6px;
    }
    p.thick {
  font-weight: bold;
  margin: 0;
  padding: 0;
}
p{
    margin: 0;
}

  
</style>
<!-- <div style="color:white;">{yScroll}</div> -->
<!-- bind:this={mainContainer} on:scroll={parseScroll} -->
<div id='mainContainer' >
    
<!-- foto1 -->
    <div class='foto'>
         <!-- <p class='thick'>TEXT</p>
         <p>subtext</p> -->
        <article><img src={image1} alt=""></article>
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
            
            <article><img src={image4} alt=""></article>
            
        </div>
<!-- extra -->


        <div>
            
            <article><img src={image6} alt=""></article>
            
        </div>
        <div>
            
            <article><img src={image5} alt=""></article>
            
        </div>
        <div>
            
            <article><img src={image4} alt=""></article>
            
        </div>
        <div>
            
            <article><img src={image6} alt=""></article>
            
        </div>




</div>
