
<script>
import image1 from "$lib/assets/1.jpg"
import image2 from "$lib/assets/2.jpg"
import image3 from "$lib/assets/3.jpg"
import image4 from "$lib/assets/4.jpg"
import image5 from "$lib/assets/5.jpg"
import image6 from "$lib/assets/6.jpg"

</script>

<style>
    #mainContainer{
        background-color:rgba(131, 146, 150, 0.6);
        height: auto;
        position: relative;
        display: flex;
        justify-content: space
        width 100vw;
        overflow-y: auto;
    }

    img{
        width: 20rem;
        height: 20rem;
        background-size: stretch;
        object-fit: cover;

    }
    div{
        /* padding: 1rem; */
        background-color: rgba(131, 146, 150, 0.6);
        justify-content: space-around
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

<div id='mainContainer'>
<!-- foto1 -->
    <div class='foto'>
         <p class='thick'>TEXT</p>
         <p>subtext</p>
        <article><img src={image1} alt=""></article>
    </div>

<!-- foto2 -->
        <div>
            <article><img src={image2} alt=""></article>
            <p class='thick'>TEXT</p>
            <p>subtext</p>
        </div>

<!-- foto3 -->
   <div class='foto'>
    <p class='thick'>TEXT</p>
         <p>subtext</p>
    <article><img src={image3} alt=""></article>
   </div>

<!-- foto4 -->
        <div class='foto'>
            
            <article><img src={image4} alt=""></article>
            <p class='thick'>TEXT</p>
                <p>subtext</p>
        </div>
<!-- extra -->




        <div>
            
            <article><img src={image4} alt=""></article>
            <p class='thick'>TEXT</p>
                <p>subtext</p>
        </div>
        <div>
            
            <article><img src={image4} alt=""></article>
            <p class='thick'>TEXT</p>
                <p>subtext</p>
        </div>
        <div>
            
            <article><img src={image4} alt=""></article>
            <p class='thick'>TEXT</p>
                <p>subtext</p>
        </div>
        <div>
            
            <article><img src={image4} alt=""></article>
            <p class='thick'>TEXT</p>
                <p>subtext</p>
        </div>




</div>
