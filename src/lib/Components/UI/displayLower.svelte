
<script>

    import { onMount , onDestroy } from "svelte";
    import image1 from "$lib/assets/1.jpg"
    import image2 from "$lib/assets/2.jpg"
    import image3 from "$lib/assets/3.jpg"
    import image4 from "$lib/assets/4.jpg"
    import image5 from "$lib/assets/5.jpg"
    import image6 from "$lib/assets/6.jpg"
    
    
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
            background-color: #205357;
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
            
            background-color: #205357;
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
      background-color: rgba(76, 200, 216, 0.564);
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
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <span class="arrow left" on:click={scrollLeft}>&lt;</span>
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <!-- svelte-ignore a11y-no-static-element-interactions -->
            <span class="arrow right" on:click={scrollRight}>&gt;</span>
    </div>
    