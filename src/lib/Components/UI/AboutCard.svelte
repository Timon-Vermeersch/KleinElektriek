<script>
  import image6 from "$lib/assets/7.jpg"
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
  font-weight:bolder;
  margin: 1rem;
  color: #ffffff;
  text-shadow: 1px 2px 5px #000000;
  

  
  
  
}
.xd{
  height: auto;
  background-color:#21929000; 
  padding: auto;
  padding-bottom: 1rem;
  padding-top: 0rem;
  margin-top: 0rem;
  
  
}

.xdd {
  
  background-color:#FFA07A; /* Bootstrap primary blue */
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

#contact {
  color:#FFA07A
}

.xdd:hover {
  background-color: #FFDAB9; /* A darker blue */
}
</style>


<div>

  <div class="card">
      <img src="{image6}" alt="">
  </div>
  <div class ="text">
      <p>Komt uw elektricien niet langs voor kleine werkjes? Neem gerust <u><a id='contact' class='contact'href="tel:+0477291260">contact</a></u> op met mij om een stopcontact of luchter te laten plaatsen, uw nieuwe poolhouse van elektriciteit te laten voorzien, ... en ondertussen hang ik snel uw nieuw kadertje op. </p>
      
    </div>
    
    <div class='xd'>
      <button class='xdd'><a href="tel:+0477291260">Nu bellen</a></button>
    </div>

  

</div>