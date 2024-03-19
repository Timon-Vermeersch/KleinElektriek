<script>
  import image6 from "$lib/assets/1-5.jpg"
  import Button from "./Button.svelte";
    

  const colorPalette = {
  darkestTeal: '#006d6d',
  mediumTeal: '#1d9a9a',
  lightTeal: '#3ac1c1',
  lightestTeal: '#54d8d8',
  brightestTeal: '#88efef'
};
  
</script>
<style>
  div{
    /* From https://css.glass */

    
    width:auto;
    height:auto;
    display: flex;
    justify-content: space-between;
    flex-direction: column; 
    overflow: hidden;
    align-items: center;
    object-fit: contain;
  }

.card{
  padding: 1rem;
  max-width: 95%;
  max-height: 95%;
  object-fit: contain;
  overflow: auto;
  
  
  
  
}

img{
  object-fit: cover;
  width: 40vh;
  height: 25vh;
  overflow: hidden;
  border-radius: 12px;
}
.text{
  background-color:#e1761e00;
  padding: auto;
  padding-bottom: 1rem;
overflow-y: scroll;}
  

p{

  font-family: 'Montserrat';
  line-height: 1.6; 
  width: auto;
  height: auto;
  padding: auto;
  font-size: large;
  
  margin: 1rem;
  color: #ffffff;
  text-shadow: 1px 2px 5px #000000;
  

  
  
  
}
.xd{
  height: auto;
  background-color:#fca53a00; 
  padding: auto;
  padding-bottom: 1rem;
  padding-top: 0rem;
  margin-top: 0rem;
  
  
}

.xdd {
  
  background-color:#ECC94B; /* Bootstrap primary blue */
  color: #0A0A0ADE;
  padding: 10px 20px;
  
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
a{
  color: #0d0d17;
}
.xdd:hover {
  background-color: #F6E05E; /* A darker blue */
}

.fullcard{
  overflow-y: auto;
}
</style>


<div class='fullcard'>

  <div class="card">
      <img src="{image6}" alt="">
  </div>
  <div class ="text">
      <p>Op zoek naar the most Complete All Round Dj? Contacteer Deejay Serge voor een unieke mix van muziekgenres die elk evenement, groot of klein, onvergetelijk maakt. Beleef een avond vol dans en plezier! <u><a href="tel:+0477291260"></a></u></p>
      
    </div>
    
    <div class='xd'>
      <button class='xdd'><a href="tel:+0477291260">Nu bellen</a></button>
</div>

  

</div>